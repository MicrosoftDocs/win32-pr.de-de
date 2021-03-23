---
title: Erstellen einer Stamm Signatur
description: Stamm Signaturen sind eine komplexe Datenstruktur, die Struktur-Strukturen enthält.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2020
ms.locfileid: "104548658"
---
# <a name="creating-a-root-signature"></a>Erstellen einer Stamm Signatur

Stamm Signaturen sind eine komplexe Datenstruktur, die Struktur-Strukturen enthält. Diese können Programm gesteuert mithilfe der unten stehenden Datenstruktur Definition definiert werden (die Methoden zum Initialisieren von Membern umfasst). Alternativ dazu können Sie in High Level Shading Language (HLSL) erstellt werden – dies bietet den Vorteil, dass der Compiler frühzeitig überprüft, ob das Layout mit dem Shader kompatibel ist.

Die API zum Erstellen einer Stamm Signatur übernimmt eine serialisierte (eigenständige, Zeiger freie) Version der layoutbeschreibung, die unten beschrieben wird. Eine Methode wird bereitgestellt, um diese serialisierte Version aus der C++-Datenstruktur zu generieren, aber eine andere Möglichkeit zum Abrufen einer serialisierten Stamm Signatur Definition besteht darin, Sie aus einem Shader abzurufen, der mit einer Stamm Signatur kompiliert wurde.

Wenn Sie Treiber Optimierungen für Stamm Signatur Deskriptoren und-Daten nutzen möchten, lesen Sie die Stamm [Signatur Version 1,1](root-signature-version-1-1.md) .

-   [Deskriptortabellenbindungstypen](#descriptor-table-bind-types)
-   [Deskriptorbereich](#descriptor-range)
-   [Deskriptortabellenlayout](#descriptor-table-layout)
-   [Stamm Konstanten](#root-constants)
-   [Stamm Deskriptor](#root-descriptor)
-   [Shader-Sichtbarkeit](#shader-visibility)
-   [Stamm Signatur Definition](#root-signature-definition)
-   [Serialisierung/Deserialisierung der Datenstruktur der Stamm Signatur](/windows)
-   [API zur Stamm Signatur Erstellung](#root-signature-creation-api)
-   [Stamm Signatur in Pipeline Zustands Objekten](#root-signature-in-pipeline-state-objects)
-   [Code zum Definieren einer Stamm Signatur der Version 1,1](#code-for-defining-a-version-11-root-signature)
-   [Verwandte Themen](#related-topics)

## <a name="descriptor-table-bind-types"></a>Deskriptortabellenbindungstypen

Der [**\_ \_ Enumerationstyp D3D12 deskriptorbereichstyp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) definiert die Typen von Deskriptoren, auf die als Teil einer deskriptortabellenlayoutdefinition verwiesen werden kann.

Es ist ein Bereich, sodass z. b., wenn ein Teil einer Deskriptortabelle 100 Srvs hat, dieser Bereich in einem Eintrag anstelle von 100 deklariert werden kann. Daher ist eine deskriptortabellendefinition eine Auflistung von Bereichen.

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

Die [**D3D12- \_ deskriptorbereichstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definiert einen Bereich von Deskriptoren eines bestimmten Typs (z. b. Srvs) innerhalb einer Deskriptortabelle.

Das- `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` Makro kann in der Regel für den- `OffsetInDescriptorsFromTableStart` Parameter des [**D3D12- \_ \_ Deskriptorbereichs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)verwendet werden. Dies bedeutet, dass der Deskriptorbereich angefügt wird, der nach dem vorherigen in der Deskriptortabelle definiert wird. Wenn die Anwendung Alias Deskriptoren haben möchte oder aus irgendeinem Grund Slots überspringen soll, kann Sie auf einen beliebigen Offset festgelegt werden `OffsetInDescriptorsFromTableStart` . Das Definieren von überlappenden Bereichen unterschiedlicher Typen ist ungültig.

Der Satz von shaderregistern, der durch die Kombination von `RangeType` ,, und angegeben wird, `NumDescriptors` `BaseShaderRegister` `RegisterSpace` kann nicht auf Deklarationen in einer Stamm Signatur mit allgemeiner [**D3D12- \_ Shader- \_ Sicht**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) Weise in Konflikt geraten bzw. überlappen.

## <a name="descriptor-table-layout"></a>Deskriptortabellenlayout

Die [**D3D12 \_ - \_ stammdeskriptortabellenstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) deklariert das Layout einer Deskriptortabelle als eine Auflistung von Deskriptorbereichen, die in einem deskriptorheap nacheinander angezeigt werden. Samplers sind in derselben Deskriptortabelle wie CBV/UAV/Srvs nicht zulässig.

Diese Struktur wird verwendet, wenn der Stammtyp des Signatur Slots auf festgelegt ist `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Verwenden Sie zum Festlegen einer Grafik (CBV-, SRV-, UAV-, Sampler-) [**Deskriptortabelle ID3D12GraphicsCommandList:: setgraphicsrootdescriptortable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Um eine COMPUTE-Deskriptortabelle festzulegen, verwenden Sie [**ID3D12GraphicsCommandList:: setcomputerootdescriptortable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Stamm Konstanten

Die Struktur der D3D12-Stamm [**\_ \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) deklariert Konstanten Inline in der Stamm Signatur, die in Shadern als ein konstanter Puffer angezeigt werden.

Diese Struktur wird verwendet, wenn der Stammtyp des Signatur Slots auf festgelegt ist `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Stamm Deskriptor

Die [**D3D12 \_ - \_ stammdeskriptorstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) deklariert Deskriptoren (die in Shadern angezeigt werden) Inline in der Stamm Signatur.

Diese Struktur wird verwendet, wenn der Stammtyp des Signatur Slots auf oder festgelegt ist `D3D12_ROOT_PARAMETER_TYPE_CBV` `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Shader-Sichtbarkeit

Der Member der [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Enumeration, die in den Shader Visibility-Parameter des [**D3D12 \_ root- \_ Parameters**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) festgelegt ist, bestimmt, welche Shader den Inhalt eines bestimmten Stamm Signatur Slots sehen. COMPUTE verwendet immer \_ alle (da es nur eine aktive Phase gibt). Grafiken können auswählen. Wenn jedoch all verwendet wird \_ , sehen alle Shader-Stufen, was an den Stamm Signatur Slot gebunden ist.

Eine Verwendung der Shader-Sichtbarkeit besteht darin, Shadern zu unterstützen, die erstellt werden, die unterschiedliche Bindungen pro Shader-Stufe mithilfe eines überlappenden Namespace erwarten Beispielsweise kann ein Vertex-Shader Folgendes deklarieren:

 

Texture2D foo: Register (T0); "

 

Außerdem kann der Pixelshader Folgendes deklarieren:

 

Texture2D Bar: Register (T0);

Wenn die Anwendung eine Stamm Signatur Bindung an T0 Visibility all vornimmt \_ , sehen beide Shader dieselbe Textur. Wenn der Shader definiert, dass jeder Shader verschiedene Texturen anzeigen soll, kann er 2 Stamm Signatur Slots mit Sichtbarkeit \_ Vertex und \_ Pixel definieren. Unabhängig von der Sichtbarkeit in einem Stamm Signatur Slot hat Sie immer die gleichen Kosten (nur in Abhängigkeit davon, was der slottype ist), bis zu einer maximalen maximalen Stamm Signatur Größe.

Bei Low-End-D3D11-Hardware \_ wird die Sichtbarkeit von Shader ebenfalls berücksichtigt, wenn die Größe von deskriptortabellen in einem Stamm Layout überprüft wird, da einige D3D11-Hardware nur eine maximale Menge an Bindungen pro Phase unterstützen kann. Diese Einschränkungen gelten nur, wenn Sie auf niedriger Ebene Hardware ausführen und nicht mehr moderne Hardware einschränken.

Wenn für eine Stamm Signatur mehrere deskriptortabellen definiert sind, die sich im Namespace gegenseitig überlappen (die Register Bindungen an den Shader) und jeder von Ihnen \_ für die Sichtbarkeit angibt, ist das Layout ungültig (bei der Erstellung tritt ein Fehler auf).

## <a name="root-signature-definition"></a>Stamm Signatur Definition

Die [**D3D12-Stamm \_ Signatur- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur kann deskriptortabellen und Inline Konstanten enthalten, die jeweils durch die D3D12-Stamm [**\_ \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Struktur und den [**\_ \_ \_ Enumerationstyp D3D12 root Parametertyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)definiert werden.

Um einen Stamm Signatur Slot zu initiieren, lesen Sie die Methoden **\* \* \* setcomputeroot** und **\* \* \* setgraphicsroot** von [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

Statische Samplern werden in der Stamm Signatur mithilfe der [**D3D12 \_ static \_ -**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) samplerstruktur beschrieben.

Eine Anzahl von Flags schränkt den Zugriff bestimmter Shader auf die Stamm Signatur ein. Weitere Informationen finden Sie unter [**D3D12 \_ root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serialisierung/Deserialisierung der Datenstruktur der Stamm Signatur

Die in diesem Abschnitt beschriebenen Methoden werden von D3D12Core.dll exportiert und stellen Methoden zum Serialisieren und Deserialisieren einer Stamm Signatur Datenstruktur bereit.

Beim Erstellen einer Stamm Signatur wird die serialisierte Form an die API übermittelt. Wenn ein Shader mit einer Stamm Signatur erstellt wurde (wenn diese Funktion hinzugefügt wird), enthält der kompilierte Shader bereits eine serialisierte Stamm Signatur.

Wenn eine Anwendung prozedurale eine [**D3D12-Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Datenstruktur generiert, muss Sie das serialisierte Formular mithilfe von [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)erstellen. Die Ausgabe von, die an [**ID3D12Device:: | aterootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)übergeben werden kann.

Wenn eine Anwendung bereits über eine serialisierte Stamm Signatur verfügt oder über einen kompilierten Shader verfügt, der eine Stamm Signatur enthält, und die Layoutdefinition Programm gesteuert ermitteln möchte (als "Reflektion" bezeichnet), kann [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) aufgerufen werden. Dadurch wird eine [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) -Schnittstelle generiert, die eine Methode zum Zurückgeben der deserialisierten [**D3D12 \_ root \_ Signature \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Datenstruktur enthält. Die-Schnittstelle besitzt die Lebensdauer der deserialisierten Datenstruktur.

## <a name="root-signature-creation-api"></a>API zur Stamm Signatur Erstellung

Die [**ID3D12Device:: kreaterootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) -API übernimmt eine serialisierte Version einer Stamm Signatur.

## <a name="root-signature-in-pipeline-state-objects"></a>Stamm Signatur in Pipeline Zustands Objekten

Die Methoden zum Erstellen des Pipeline Zustands ([**ID3D12Device:: anategraphicspipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) und [**ID3D12Device:: aufgabencomputepipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) akzeptieren eine optionale [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) -Schnittstelle als Eingabeparameter (gespeichert in einer [**D3D12- \_ Grafik \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) -Struktur). Dadurch wird jede bereits in den Shadern bereits Stamm Signatur überschrieben.

Wenn eine Stamm Signatur an eine der Create Pipeline State-Methoden übergeben wird, wird diese Stamm Signatur anhand aller Shader in der PSO aus Kompatibilitätsgründen überprüft und an den Treiber übergeben, der für alle Shader verwendet werden soll. Wenn einer der Shader eine andere Stamm Signatur aufweist, wird er durch die an der API über gegebene Stamm Signatur ersetzt. Wenn eine Stamm Signatur nicht übergeben wird, müssen alle an übergebenen Shader über eine Stamm Signatur verfügen, und Sie müssen mit – versehen werden. Durch das Festlegen eines PSO in einer Befehlsliste oder eines Pakets wird die Stamm Signatur nicht geändert. Dies wird durch die Methoden [**setgraphicsrootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) und [**setcomputerootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)erreicht. Wenn/Dispatch (Compute) aufgerufen wird, muss die Anwendung sicherstellen, dass das aktuelle PSO mit der aktuellen Stamm Signatur übereinstimmt. Andernfalls ist das Verhalten nicht definiert.

## <a name="code-for-defining-a-version-11-root-signature"></a>Code zum Definieren einer Stamm Signatur der Version 1,1

Im folgenden Beispiel wird gezeigt, wie eine Stamm Signatur im folgenden Format erstellt wird:



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **Rootparameterindex** | **Contents**                                   |                                              |
| \[0\]                  | Stamm Konstanten: {B2}                         | (1 CBV)                                      |
| \[1\]                  | Deskriptortabelle: {T2-T7, U0-U3}             | (6 Srvs + 4 UAVs)                            |
| \[2\]                  | Root CBV: {B0}                               | (1 CBV, statische Daten)                         |
| \[3\]                  | Deskriptortabelle: {S0-S1}                    | (2 Samplers)                                 |
| \[4\]                  | Deskriptortabelle: {T8-ungebunden}           | (ungebunden \# von Srvs, flüchtige Deskriptoren) |
| \[5\]                  | Deskriptortabelle: {(T0, festplattenspeicher1)-ungebunden} | (ungebunden \# von Srvs, flüchtige Deskriptoren) |
| \[6\]                  | Deskriptortabelle: {B1}                       | (1 CBV, statische Daten)                         |



 

Wenn die meisten Teile der Stamm Signatur in den meisten Fällen verwendet werden, kann es besser sein, die Stamm Signatur zu häufig zu ändern. Anwendungen sollten Einträge in der Stamm Signatur von der am häufigsten zu den geringsten Änderungen sortieren. Wenn eine APP die Bindungen in einen beliebigen Teil der Stamm Signatur ändert, muss der Treiber möglicherweise eine Kopie des root-Signatur Zustands erstellen, was zu nicht trivialen Kosten werden kann, wenn er über viele Zustandsänderungen hinweg multipliziert wird.

Außerdem wird durch die Stamm Signatur ein statischer Sampler definiert, der die anisotrope Textur Filterung im Shader-Register S3 durchführt.

Nachdem diese Stamm Signatur gebunden ist, können deskriptortabellen, root CBV und Konstanten dem \[ Parameter Bereich 0.. 6 zugewiesen werden \] . Beispielsweise können deskriptortabellen (Bereiche in einem deskriptorheap) an jeden der Stamm Parameter \[ 1 \] und \[ 3.. 6 gebunden \] werden.

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

Der folgende Code veranschaulicht, wie die obige Stamm Signatur in einer Grafik Befehlsliste verwendet werden kann.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
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

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> <dt>

[Angeben von Stamm Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Verwenden einer Stamm Signatur](using-a-root-signature.md)
</dt> </dl>

 

 
