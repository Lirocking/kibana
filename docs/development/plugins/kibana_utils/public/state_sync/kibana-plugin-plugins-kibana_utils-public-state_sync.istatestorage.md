<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [kibana-plugin-plugins-kibana\_utils-public-state\_sync](./kibana-plugin-plugins-kibana_utils-public-state_sync.md) &gt; [IStateStorage](./kibana-plugin-plugins-kibana_utils-public-state_sync.istatestorage.md)

## IStateStorage interface

Any StateStorage have to implement IStateStorage interface StateStorage is responsible for: \* state serialisation / deserialization \* persisting to and retrieving from storage

For an example take a look at already implemented [IKbnUrlStateStorage](./kibana-plugin-plugins-kibana_utils-public-state_sync.ikbnurlstatestorage.md) and [ISessionStorageStateStorage](./kibana-plugin-plugins-kibana_utils-public-state_sync.isessionstoragestatestorage.md) state storages

<b>Signature:</b>

```typescript
export interface IStateStorage 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [cancel](./kibana-plugin-plugins-kibana_utils-public-state_sync.istatestorage.cancel.md) | <code>() =&gt; void</code> | Optional method to cancel any pending activity [syncState()](./kibana-plugin-plugins-kibana_utils-public-state_sync.syncstate.md) will call it during destroy, if it is provided by IStateStorage |
|  [change$](./kibana-plugin-plugins-kibana_utils-public-state_sync.istatestorage.change_.md) | <code>&lt;State = unknown&gt;(key: string) =&gt; Observable&lt;State &#124; null&gt;</code> | Should notify when the stored state has changed |
|  [get](./kibana-plugin-plugins-kibana_utils-public-state_sync.istatestorage.get.md) | <code>&lt;State = unknown&gt;(key: string) =&gt; State &#124; null</code> | Should retrieve state from the storage and deserialize it |
|  [set](./kibana-plugin-plugins-kibana_utils-public-state_sync.istatestorage.set.md) | <code>&lt;State&gt;(key: string, state: State) =&gt; any</code> | Take in a state object, should serialise and persist |

