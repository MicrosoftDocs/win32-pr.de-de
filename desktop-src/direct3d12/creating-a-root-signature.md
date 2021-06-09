---
title: Erstellen einer Stammsignatur
description: Stammsignaturen sind eine komplexe Datenstruktur, die geschachtelte Strukturen enthält.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87209dfc324b950a74d2b31e5f1a1f6326792b9f
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826436"
---
# <a name="creating-a-root-signature"></a>Erstellen einer Stammsignatur

Stammsignaturen sind eine komplexe Datenstruktur, die geschachtelte Strukturen enthält. Diese können programmgesteuert mithilfe der unten angegebenen Datenstrukturdefinition definiert werden (einschließlich Methoden zum Initialisieren von Membern). Alternativ können sie in HLSL (High Level Shading Language) erstellt werden. Dies hat den Vorteil, dass der Compiler frühzeitig überprüft, ob das Layout mit dem Shader kompatibel ist.

Die API zum Erstellen einer Stammsignatur verwendet eine serialisierte (eigenständige, zeigerfreie) Version der unten beschriebenen Layoutbeschreibung. Eine Methode wird zum Generieren dieser serialisierten Version aus der C++-Datenstruktur bereitgestellt. Eine weitere Möglichkeit zum Abrufen einer serialisierten Stammsignaturdefinition besteht jedoch darin, sie von einem Shader abzurufen, der mit einer Stammsignatur kompiliert wurde.

Wenn Sie Treiberoptimierungen für Stammsignaturdeskriptoren und -daten nutzen möchten, lesen Sie [Stammsignaturversion 1.1.](root-signature-version-1-1.md)

-   [Deskriptortabellenbindungstypen](#descriptor-table-bind-types)
-   [Deskriptorbereich](#descriptor-range)
-   [Deskriptortabellenlayout](#descriptor-table-layout)
-   [Stammkonstanten](#root-constants)
-   [Stammdeskriptor](#root-descriptor)
-   [Shadersichtbarkeit](#shader-visibility)
-   [Stammsignaturdefinition](#root-signature-definition)
-   [Serialisierung/Deserialisierung der Stammsignaturdatenstruktur](/windows)
-   [API zum Erstellen von Stammsignaturen](#root-signature-creation-api)
-   [Stammsignatur in Pipelinezustandsobjekten](#root-signature-in-pipeline-state-objects)
-   [Code zum Definieren einer Stammsignatur der Version 1.1](#code-for-defining-a-version-11-root-signature)
-   [Verwandte Themen](#related-topics)

## <a name="descriptor-table-bind-types"></a>Deskriptortabellenbindungstypen

Die Enumeration [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) definiert die Typen von Deskriptoren, auf die als Teil einer Deskriptortabellenlayoutdefinition verwiesen werden kann.

Es handelt sich um einen Bereich, sodass dieser Bereich beispielsweise in einem Eintrag deklariert werden kann, wenn ein Teil einer Deskriptortabelle 100 SRVs enthält, anstatt in 100. Eine Deskriptortabellendefinition ist also eine Auflistung von Bereichen.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Deskriptorbereich

Die [**D3D12 \_ DESCRIPTOR \_ RANGE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definiert einen Deskriptorbereich eines bestimmten Typs (z. B. SRVs) innerhalb einer Deskriptortabelle.

Das `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` Makro kann in der Regel für den `OffsetInDescriptorsFromTableStart` -Parameter von [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)verwendet werden. Dies bedeutet, dass sie den Deskriptorbereich anfügen, der nach dem vorherigen in der Deskriptortabelle definiert wird. Wenn die Anwendung Aliasdeskriptoren verwenden oder Aus irgendeinem Grund Slots überspringen möchte, kann sie `OffsetInDescriptorsFromTableStart` auf den gewünschten Offset festlegen. Das Definieren überlappender Bereiche verschiedener Typen ist ungültig.

Der Satz von Shaderregistern, die durch die Kombination von , , und angegeben werden, `RangeType` kann keine Konflikte oder `NumDescriptors` `BaseShaderRegister` `RegisterSpace` Überschneidungen zwischen Deklarationen in einer Stammsignatur mit allgemeiner [**D3D12-SHADER-SICHTBARKEIT \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) verursachen (weitere Informationen finden Sie im Abschnitt zur Shadersichtbarkeit weiter unten).

## <a name="descriptor-table-layout"></a>Deskriptortabellenlayout

Die [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) deklariert das Layout einer Deskriptortabelle als Auflistung von Deskriptorbereichen, die nacheinander in einem Deskriptorheap angezeigt werden. Sampler sind in derselben Deskriptortabelle nicht zulässig wie CBV/UAV/SRVs.

Diese Struktur wird verwendet, wenn der Stammsignaturslottyp auf festgelegt `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` ist.

Um eine Grafikdeskriptortabelle (CBV, SRV, UAV, Sampler) festzulegen, verwenden Sie [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Um eine Computedeskriptortabelle festzulegen, verwenden Sie [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Stammkonstanten

Die [**D3D12 \_ ROOT \_ CONSTANTS-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) deklariert Konstanten inline in der Stammsignatur, die in Shadern als ein Konstantenpuffer angezeigt werden.

Diese Struktur wird verwendet, wenn der Stammsignaturslottyp auf festgelegt `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` ist.

## <a name="root-descriptor"></a>Stammdeskriptor

Die [**D3D12 \_ ROOT \_ DESCRIPTOR-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) deklariert Deskriptoren (die in Shadern angezeigt werden) inline in der Stammsignatur.

Diese Struktur wird verwendet, wenn der Stammsignaturslottyp auf oder festgelegt `D3D12_ROOT_PARAMETER_TYPE_CBV` `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` ist.

## <a name="shader-visibility"></a>Shadersichtbarkeit

Der Member der [**D3D12 \_ SHADER \_ VISIBILITY-Enumeration,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) die im Shader-Sichtbarkeitsparameter von [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) festgelegt ist, bestimmt, welche Shader den Inhalt eines angegebenen Stammsignaturslots sehen. Compute verwendet immer \_ ALL (da es nur eine aktive Phase gibt). Grafiken können auswählen, aber wenn all verwendet \_ wird, sehen alle Shaderstufen, was am Stammsignaturslot gebunden ist.

Eine Verwendung der Shadersichtbarkeit ist die Unterstützung von Shadern, die erstellt wurden und unterschiedliche Bindungen pro Shaderphase mithilfe eines überlappenden Namespace erwarten. Beispielsweise kann ein Vertex-Shader Folgendes deklarieren:

```hlsl
Texture2D foo : register(t0);
```

und der Pixelshader kann auch Folgendes deklarieren:

```hlsl
Texture2D bar : register(t0);
```

Wenn die Anwendung eine Stammsignaturbindung an t0 VISIBILITY \_ ALL vornimmt, sehen beide Shader die gleiche Textur. Wenn der Shader definiert, dass jeder Shader tatsächlich unterschiedliche Texturen anzeigen soll, kann er zwei Stammsignaturslots mit VISIBILITY \_ VERTEX und \_ PIXEL definieren. Unabhängig von der Sichtbarkeit eines Stammsignaturslots sind die Kosten (kosten nur je nach SlotType) für eine feste maximale Stammsignaturgröße identisch.

Bei Low-End-D3D11-Hardware wird SHADER \_ VISIBILITY auch beim Überprüfen der Größe von Deskriptortabellen in einem Stammlayout berücksichtigt, da einige D3D11-Hardware nur eine maximale Anzahl von Bindungen pro Phase unterstützen kann. Diese Einschränkungen gelten nur, wenn sie auf Low-Tier-Hardware ausgeführt werden, und beschränken überhaupt keine modernere Hardware.

Wenn für eine Stammsignatur mehrere Deskriptortabellen definiert sind, die sich im Namespace überlappen (die Registerbindungen an den Shader), und eine davon \_ all für die Sichtbarkeit angibt, ist das Layout ungültig (die Erstellung schlägt fehl).

## <a name="root-signature-definition"></a>Stammsignaturdefinition

Die [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) kann Deskriptortabellen und Inlinekonstanten enthalten, wobei jeder Slottyp durch die [**D3D12 \_ ROOT \_ PARAMETER-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) und die Enumeration [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)definiert wird.

Informationen zum Initiieren eines Stammsignaturslots finden Sie in den Methoden **SetComputeRoot \* \* \*** und **\* \* \* SetGraphicsRoot** von [**ID3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

Statische Sampler werden in der Stammsignatur mithilfe der [**D3D12 \_ STATIC \_ SAMPLER-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) beschrieben.

Eine Reihe von Flags schränkt den Zugriff bestimmter Shader auf die Stammsignatur ein. Weitere Informationen finden Sie unter [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serialisierung/Deserialisierung der Stammsignaturdatenstruktur

Die in diesem Abschnitt beschriebenen Methoden werden von D3D12Core.dll exportiert und stellen Methoden zum Serialisieren und Deserialisieren einer Stammsignaturdatenstruktur bereit.

Das serialisierte Formular wird beim Erstellen einer Stammsignatur an die API übergeben. Wenn ein Shader mit einer Stammsignatur erstellt wurde (wenn diese Funktion hinzugefügt wird), enthält der kompilierte Shader bereits eine serialisierte Stammsignatur.

Wenn eine Anwendung prozedural eine [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC-Datenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) generiert, muss sie das serialisierte Formular mithilfe von [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)erstellen. Die Ausgabe von , die an [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)übergeben werden kann.

Wenn eine Anwendung bereits über eine serialisierte Stammsignatur verfügt oder über einen kompilierten Shader verfügt, der eine Stammsignatur enthält und die Layoutdefinition programmgesteuert ermitteln möchte (als "Reflektion" bezeichnet), kann [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) aufgerufen werden. Dadurch wird eine [**ID3D12RootSignatureDeserializer-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) generiert, die eine Methode zum Zurückgeben der deserialisierten [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC-Datenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) enthält. Die Schnittstelle besitzt die Lebensdauer der deserialisierten Datenstruktur.

## <a name="root-signature-creation-api"></a>API zum Erstellen von Stammsignaturen

Die [**ID3D12Device::CreateRootSignature-API**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) übernimmt eine serialisierte Version einer Stammsignatur.

## <a name="root-signature-in-pipeline-state-objects"></a>Stammsignatur in Pipelinezustandsobjekten

Die Methoden zum Erstellen des Pipelinezustands ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) und [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) verwenden eine optionale [**ID3D12RootSignature-Schnittstelle**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) als Eingabeparameter (gespeichert in einer [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC-Struktur).**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) Dadurch werden alle Stammsignaturen überschrieben, die bereits in den Shadern enthalten sind.

Wenn eine Stammsignatur an eine der Methoden zum Erstellen des Pipelinezustands übergeben wird, wird diese Stammsignatur für alle Shader im PSO auf Kompatibilität überprüft und dem Treiber zur Verwendung mit allen Shadern übergeben. Wenn einer der Shader eine andere Stammsignatur enthält, wird er durch die an die API übergebene Stammsignatur ersetzt. Wenn keine Stammsignatur übergeben wird, müssen alle übergebenen Shader über eine Stammsignatur verfügen, und sie müssen übereinstimmen. Dies wird dem Treiber übergeben. Das Festlegen eines PSO für eine Befehlsliste oder ein Paket ändert die Stammsignatur nicht. Dies wird mit den Methoden [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) und [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)erreicht. Wenn draw(graphics)/dispatch(compute) aufgerufen wird, muss die Anwendung sicherstellen, dass die aktuelle PSO mit der aktuellen Stammsignatur übereinstimmt. Andernfalls ist das Verhalten nicht definiert.

## <a name="code-for-defining-a-version-11-root-signature"></a>Code zum Definieren einer Stammsignatur der Version 1.1

Das folgende Beispiel zeigt, wie Sie eine Stammsignatur im folgenden Format erstellen:



| RootParameterIndex                       | Inhalte                                               | Werte                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| \[0\]                  | Stammkonstanten: { b2 }                         | (1 CBV)                                      |
| \[1\]                  | Deskriptortabelle: { t2-t7, u0-u3 }             | (6 SRVs + 4 UAVs)                            |
| \[2\]                  | Stamm-CBV: { b0 }                               | (1 CBV, statische Daten)                         |
| \[3\]                  | Deskriptortabelle: { s0-s1 }                    | (2 Sampler)                                 |
| \[4\]                  | Deskriptortabelle: { t8 – ungebunden }           | (ungebunden \# von SRVs, flüchtige Deskriptoren) |
| \[5\]                  | Deskriptortabelle: { (t0, space1) - unbounded } | (ungebunden \# von SRVs, flüchtige Deskriptoren) |
| \[6\]                  | Deskriptortabelle: { b1 }                       | (1 CBV, statische Daten)                         |



 

Wenn die meisten Teile der Stammsignatur meistens verwendet werden, kann dies besser sein, als die Stammsignatur zu häufig wechseln zu müssen. Anwendungen sollten Einträge in der Stammsignatur von den am häufigsten geänderten in die geringsten Einträge sortieren. Wenn eine App die Bindungen an einen beliebigen Teil der Stammsignatur ändert, muss der Treiber möglicherweise eine Kopie eines oder aller Stammsignaturstatus erstellen. Dies kann zu nicht typischen Kosten werden, wenn er mit vielen Zustandsänderungen multipliziert wird.

Darüber hinaus definiert die Stammsignatur einen statischen Sampler, der anisotrope Texturfilterung im Shaderregister s3 vorsetzt.

Nachdem diese Stammsignatur gebunden wurde, können Deskriptortabellen, CBV-Stammtabellen und Konstanten dem \[ Parameterbereich 0..6 zugewiesen \] werden. Beispielsweise können Deskriptortabellen (Bereiche in einem Deskriptorheap) an jeden der Stammparameter \[ 1 \] und \[ 3..6 gebunden \] werden.

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

Der folgende Code veranschaulicht, wie die obige Stammsignatur in einer Grafikbefehlsliste verwendet werden kann.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(2,pHeaps);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stammsignaturen](root-signatures.md)
</dt> <dt>

[Festlegen von Stammsignaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Verwenden einer Stammsignatur](using-a-root-signature.md)
</dt> </dl>

 

 
