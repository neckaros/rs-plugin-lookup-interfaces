Interfaces for episodes/movies/Actors... and Media Lookup

Like every other plugins you must implement an info request

````
#[plugin_fn]
pub fn infos() -> FnResult<Json<PluginInformation>> {
    Ok(Json(
        PluginInformation { name: "xxxx_request".into(), kind: PluginType::Lookup, version: 1, publisher: "neckaros".into(), description: "descruption".into(), credential_kind: Some(CredentialType::Token), ..Default::default() }
    ))
}
```