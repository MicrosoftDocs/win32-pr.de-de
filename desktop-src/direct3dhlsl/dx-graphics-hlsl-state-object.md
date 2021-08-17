---
title: Statusobjekte
description: Verwenden Sie HLSL, um Zustandsobjekte zu definieren.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70ff3ca1fb2509cd5f788cc1965920c46af5791bec10bb833df19f4b4f9be533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119934"
---
# <a name="state-objects"></a>Statusobjekte

Mit Shadermodellen 6.3 und höher verfügen Anwendungen über die Einfachheit und Flexibilität, DXR-Zustandsobjekte zusätzlich zur Verwendung von Direct3D 12-APIs direkt im HLSL-Shadercode definieren zu können.

In HLSL werden Zustandsobjekte mit dieser Syntax deklariert:

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Typ**<br/>     | Identifiziert den Typ des Unterobjekts. Muss einer der unterstützten HLSL-Unterobjekttypen sein.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**<br/> | Felder des Unterobjekts. Im Folgenden werden bestimmte Felder für jeden Unterobjekttyp beschrieben.<br/> |




Liste der Unterobjekttypen:
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

Der StateObjectConfig-Unterobjekttyp entspricht [einer](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) D3D12_STATE_OBJECT_CONFIG Struktur.

Es verfügt über ein Feld, ein bitweises Flag, das ein oder beides von ist.

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

## <a name="globalrootsignature"></a>GlobalRootSignature
Eine GlobalRootSignature entspricht [einer](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) D3D12_GLOBAL_ROOT_SIGNATURE Struktur.

Die Felder bestehen aus einer Reihe von Zeichenfolgen, die die Teile der Stammsignatur beschreiben. Weitere Informationen hierzu finden Sie unter [Angeben von Stammsignaturen in HLSL.](../direct3d12/specifying-root-signatures-in-hlsl.md)

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

## <a name="localrootsignature"></a>LocalRootSignature
Eine LocalRootSignature entspricht [einer](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) D3D12_LOCAL_ROOT_SIGNATURE Struktur.

Genau wie das globale Stammsignatur-Unterobjekt bestehen die Felder aus einer Reihe von Zeichenfolgen, die die Teile der Stammsignatur beschreiben. Weitere Informationen hierzu finden Sie unter [Angeben von Stammsignaturen in HLSL.](../direct3d12/specifying-root-signatures-in-hlsl.md)

Beispiel:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
Standardmäßig kann ein Unterobjekt, das lediglich in derselben Bibliothek wie ein Export deklariert ist, auf diesen Export angewendet werden. Anwendungen haben jedoch die Möglichkeit, dies zu überschreiben und genau zu erfahren, welches Unterobjekt mit welchem Export verwendet wird. In HLSL erfolgt diese "explizite Zuordnung" mithilfe von SubobjectToExportsAssocation.

Eine SubobjectToExportsAssocation entspricht [einer ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION Struktur.

Dieses Unterobjekt wird mit der Syntax deklariert.

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**<br/>     | Eine Zeichenfolge, die ein exportiertes Unterobjekt identifiziert.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exportiert**<br/> | Eine Zeichenfolge, die eine durch Semikolons getrennte Liste von Exporten enthält.<br/> |


Beispiel:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Beachten Sie, dass beide Felder *exportierte Namen* verwenden. Ein exportierter Name kann sich vom ursprünglichen Namen in HLSL unterscheiden, wenn sich die Anwendung für das Umbenennen des Exports entscheidet.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

Ein RaytracingShaderConfig-Wert entspricht [einer](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) D3D12_RAYTRACING_SHADER_CONFIG Struktur.

Dieses Unterobjekt wird mit der Syntax deklariert.

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Numerischer Wert für den maximalen Speicher für Skalarwerte (jeweils 4 Byte) in Raynutzlasten für zugeordnete Raytracing-Shader.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Numerischer Wert für die maximale Anzahl von Skalaren (jeweils als 4 Byte gezählt), die für Attribute in zugeordneten Raytracing-Shadern verwendet werden können. Der Wert darf den Wert [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES.](../direct3d12/constants.md)<br/> |


Beispiel:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

Eine RaytracingPipelineConfig entspricht [einer](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) D3D12_RAYTRACING_PIPELINE_CONFIG Struktur.

Dieses Unterobjekt wird mit der Syntax deklariert.

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Numerisches Limit, das für die Ray-Rekursion in der Raytracingpipeline verwendet werden soll. Dabei handelt es sich um eine Zahl zwischen 0 und 31 (einschließlich). <br/> |


Beispiel:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Da für die Raytracing-Rekursion Leistungskosten entstehen, sollten Anwendungen die niedrigste Rekursionstiefe verwenden, die für die gewünschten Ergebnisse erforderlich ist.

Wenn Shaderaufrufe die maximale Rekursionstiefe noch nicht erreicht haben, können sie [TraceRay](../direct3d12/traceray-function.md) so oft aufrufen. Wenn sie jedoch die maximale Rekursionstiefe erreichen oder überschreiten, versetzt der Aufruf von TraceRay das Gerät in den entfernten Zustand. Daher sollten Raytracing-Shader darauf achten, den Aufruf von TraceRay zu beenden, wenn sie die maximale Rekursionstiefe erreicht oder überschritten haben.

## <a name="trianglehitgroup"></a>TriangleHitGroup

Eine TriangleHitGroup entspricht [](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) einer D3D12_HIT_GROUP_DESC-Struktur, deren Type-Feld auf [D3D12_HIT_GROUP_TYPE_TRIANGLES.](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)

Dieses Unterobjekt wird mit der Syntax deklariert.

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Zeichenfolgenname des anyhit-Shaders für die Treffergruppe oder eine leere Zeichenfolge.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Zeichenfolgenname des nächstgelegenen Treffer-Shaders für die Treffergruppe oder eine leere Zeichenfolge.<br/> |


Beispiel:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Beachten Sie, dass beide Felder *exportierte Namen* verwenden. Ein exportierter Name kann sich vom ursprünglichen Namen in HLSL unterscheiden, wenn sich die Anwendung für das Umbenennen des Exports entscheidet.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Eine ProceduralPrimitiveHitGroup entspricht einer [D3D12_HIT_GROUP_DESC-Struktur,](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) deren Type-Feld auf [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)festgelegt ist.

Dieses Unterobjekt wird mit der Syntax deklariert.

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Element                                                                                         | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**<br/>     | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Zeichenfolgenname des Anyhit-Shaders für die Treffergruppe oder eine leere Zeichenfolge.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Zeichenfolgenname des nächstgelegenen Treffer-Shaders für die Treffergruppe oder eine leere Zeichenfolge.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Zeichenfolgenname des Schnittmengen-Shaders für die Treffergruppe oder eine leere Zeichenfolge.<br/> |


Beispiel:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Beachten Sie, dass die drei Felder *exportierte* Namen verwenden. Ein exportierter Name kann sich vom ursprünglichen Namen in HLSL unterscheiden, wenn sich die Anwendung für das Umbenennen des Exports entscheidet.

## <a name="remarks"></a>Hinweise

Unterobjekte haben das Konzept "zuordnung" oder "welches Unterobjekt mit welchem Export".

Bei der Angabe von Unterobjekten über Shadercode folgt die Auswahl von "welches Unterobjekt mit welchem Export" den Regeln, wie in der [DXR-Spezifikation](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior)beschrieben. Nehmen wir insbesondere an, dass eine Anwendung über einen Export verfügt. Wenn eine Anwendung den Export mit der Stammsignatur A über Shadercode und der Stammsignatur B über Anwendungscode zuweist, wird B verwendet. Der Entwurf von "Use B" anstelle von "produce an error" bietet Anwendungen die Möglichkeit, DXIL-Zuordnungen bequem mithilfe von Anwendungscode zu überschreiben, anstatt gezwungen zu werden, Shader neu zu kompilieren, um nicht übereinstimmende Dinge aufzulösen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Entwicklerblogbeitrag "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects" (Neu in D3D12 – DirectX Raytracing (DXR) unterstützt jetzt Bibliotheksunterobjekte)](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[DirectX Raytracing (DXR) – Funktionale Spezifikation](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Beispiel: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>