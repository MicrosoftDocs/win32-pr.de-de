---
title: Statusobjekte
description: Verwenden Sie HLSL zum Definieren von Zustands Objekten.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995286"
---
# <a name="state-objects"></a>Statusobjekte

Mit Shader-Modellen 6,3 und höher haben Anwendungen die Möglichkeit, DXR-Zustands Objekte direkt in HLSL-Shader-Code zu definieren, zusätzlich zur Verwendung von Direct3D 12-APIs.

In HLSL werden Zustands Objekte mit der folgenden Syntax deklariert:

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**<br/>     | Identifiziert den Typ des untergeordneten Objekts. Muss einer der unterstützten HLSL-untergeordneten Typen sein.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Feld [1, 2,...]**<br/> | Felder des unter Objekts. Bestimmte Felder für jeden Typ von untergeordneten Objekten werden im folgenden beschrieben.<br/> |




Liste der untergeordneten Typen:
-   [Stateobjectconfig](#stateobjectconfig)
-   [Globalrootsignature](#globalrootsignature)
-   [Localrootsignature](#localrootsignature)
-   [Subobjectjeexportsassokation](#subobjecttoexportsassocation)
-   [Raytracingshaderconfig](#raytracingshaderconfig)
-   [Raytracingpipelineconfig](#raytracingpipelineconfig)
-   ["Testgruppe"](#trianglehitgroup)
-   [Prozelinialprimitivehitgroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>Stateobjectconfig

Der untergeordnete Typ des stateobjectconfig-Objekts entspricht einer [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) -Struktur.

Sie verfügt über ein Feld, ein bitweises Flag, das eine oder beide von ist.

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

oder 0 (null) für keines von beiden.

Beispiel:

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>Globalrootsignature
Eine globalrootsignature entspricht einer [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) Struktur.

Die Felder bestehen aus einer Reihe von Zeichen folgen, die die Teile der Stamm Signatur beschreiben. Weitere Informationen hierzu finden Sie unter [Angeben von Stamm Signaturen in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Beispiel:
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>Localrootsignature
Eine localrootsignature entspricht einer [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) Struktur.

Genau wie das untergeordnete Stamm Signatur Objekt bestehen die Felder aus einer Reihe von Zeichen folgen, die die Teile der Stamm Signatur beschreiben. Weitere Informationen hierzu finden Sie unter [Angeben von Stamm Signaturen in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Beispiel:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>Subobjectjeexportsassokation
Standardmäßig kann ein untergeordnetes Objekt, das nur in derselben Bibliothek wie ein Export deklariert ist, auf diesen Export angewendet werden. Anwendungen sind jedoch in der Lage, diese außer Kraft zu setzen und spezifische Informationen darüber zu erhalten, was das untergeordnete Objekt mit welchem Export ist. In HLSL wird diese "explizite Zuordnung" mithilfe von "SubObject-exportsassocation" durchgeführt.

Ein subobjecttexportsassoationentspricht einer [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) Struktur.

Dieses untergeordnete Objekt wird mit der Syntax deklariert.

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**Subobjectname**<br/>     | Eine Zeichenfolge, die ein exportiertes unter Objekt identifiziert.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Ö**<br/> | Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der Exporte enthält.<br/> |


Beispiel:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Beachten Sie, dass beide Felder *exportierte* Namen verwenden. Ein exportierter Name unterscheidet sich möglicherweise vom ursprünglichen Namen in HLSL, wenn die Anwendung die Export Umbenennung auswählt.

## <a name="raytracingshaderconfig"></a>Raytracingshaderconfig

Ein raytracingshaderconfig entspricht einer [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) Struktur.

Dieses untergeordnete Objekt wird mit der Syntax deklariert.

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**Maxpayloadsize**<br/>     | Numerischer Wert für den maximalen Speicherplatz für skalare (jeweils als 4 Bytes gezählt) in Ray-Nutzlasten für zugeordnete Raytracing-Shader.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**Maxattributesize**<br/> | Numerischer Wert für die maximale Anzahl von skalaren (jeweils als 4 Bytes gezählt), die für Attribute in zugeordneten Raytracing-Shadern verwendet werden kann. Der Wert darf [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md)nicht überschreiten.<br/> |


Beispiel:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>Raytracingpipelineconfig

Ein raytracingpipelineconfig entspricht einer [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) Struktur.

Dieses untergeordnete Objekt wird mit der Syntax deklariert.

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**Maxtracerecursiontiefe**<br/>     | Numerischer Grenzwert für die Ray-Rekursion in der Raytracing-Pipeline. Dabei handelt es sich um eine Zahl zwischen 0 und einschließlich 31. <br/> |


Beispiel:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Da für die Raytracing-Rekursion Leistungskosten anfallen, sollten Anwendungen die niedrigste Rekursions Tiefe verwenden, die für die gewünschten Ergebnisse erforderlich ist.

Wenn Shader-Aufrufe die maximale Rekursions Tiefe noch nicht erreicht haben, können Sie [traceray](../direct3d12/traceray-function.md) beliebig oft aufrufen. Wenn die maximale Rekursions Tiefe erreicht oder überschritten wird, versetzt der Aufruf von traceray das Gerät in den entfernten Zustand. Daher sollten Raytracing-Shader darauf achten, den Aufruf von traceray zu unterbinden, wenn Sie die maximale Rekursions Tiefe erreicht oder überschritten haben.

## <a name="trianglehitgroup"></a>"Testgruppe"

Eine "zanglehitgroup" entspricht einer [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) -Struktur, deren Type-Feld auf " [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)" festgelegt ist.

Dieses untergeordnete Objekt wird mit der Syntax deklariert.

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**Anyhitshader**<br/>     | Der Zeichen folgen Name des anyhit-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**Closesthitshader**<br/> | Der Zeichen folgen Name des nächstgelegenen Treffer-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.<br/> |


Beispiel:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Beachten Sie, dass beide Felder *exportierte* Namen verwenden. Ein exportierter Name unterscheidet sich möglicherweise vom ursprünglichen Namen in HLSL, wenn die Anwendung die Export Umbenennung auswählt.

## <a name="proceduralprimitivehitgroup"></a>Prozelinialprimitivehitgroup

Eine "prozebegruppe" ist eine [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) Struktur, deren Type-Feld auf " [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)" festgelegt ist.

Dieses untergeordnete Objekt wird mit der Syntax deklariert.

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Element                                                                                         | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**Anyhitshader**<br/>     | Der Zeichen folgen Name des anyhit-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**Closesthitshader**<br/> | Der Zeichen folgen Name des nächstgelegenen Treffer-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**Intersectionshader**<br/> | Der Zeichen folgen Name des Schnittstellen Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.<br/> |


Beispiel:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Beachten Sie, dass in den drei Feldern *exportierte* Namen verwendet werden. Ein exportierter Name unterscheidet sich möglicherweise vom ursprünglichen Namen in HLSL, wenn die Anwendung die Export Umbenennung auswählt.

## <a name="remarks"></a>Bemerkungen

Untergeordnete Objekte haben das Konzept "Association" oder "welches unter Objekt mit welchem Export".

Beim Angeben von untergeordneten Elementen über den Shader-Code befolgt die Auswahl des untergeordneten Objekts, mit dem der Export erfolgt, den Regeln entsprechend den [Angaben in der DXR-Spezifikation](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). Stellen Sie sich vor, dass eine Anwendung über einen Export verfügt. Wenn eine Anwendung den Export mit der Stamm Signatur a über Shader-Code und Stamm Signatur B über den Anwendungscode zuordnet, ist B der Wert, der verwendet wird. Der Entwurf von "Use B" anstelle von "Fehler verursachen" gibt Anwendungen die Möglichkeit, dxil-Zuordnungen mithilfe von Anwendungscode bequem zu überschreiben, anstatt Shader erneut zu kompilieren, um nicht übereinstimmende Elemente aufzulösen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Entwickler-Blog Beitrag "New in D3D12 – DirectX Raytracing (DXR) unterstützt jetzt Bibliotheks-unter Objekte"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Funktionsspezifikation für DirectX-Raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Beispiel: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>