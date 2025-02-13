
# pyvider/rpcplugin/types.py

from typing import TypeVar, TypeAlias, Protocol, Any, Dict, Union
from grpc.aio import Server as GRPCServer

# Core Protocol Types
class SerializableT(Protocol):
    """Protocol for objects that can be serialized to/from dict."""
    def to_dict(self) -> Dict[str, Any]: ...
    @classmethod
    def from_dict(cls, data: Dict[str, Any]) -> 'SerializableT': ...

# Core Type Variables
ConfigT = TypeVar('ConfigT', bound='RPCPluginConfig')
HandlerT = TypeVar('HandlerT', bound='RPCPluginHandler')
ProtocolT = TypeVar('ProtocolT', bound='RPCPluginProtocol')
TransportT = TypeVar('TransportT', bound='RPCPluginTransport')
ServerT = TypeVar('ServerT', bound=GRPCServer)

# Common Return Types
ResultT = TypeVar('ResultT')
ErrorT = TypeVar('ErrorT', bound=Exception)