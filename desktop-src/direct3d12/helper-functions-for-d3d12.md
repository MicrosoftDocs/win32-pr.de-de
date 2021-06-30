---
title: Funktionen des Hilfsprogramms für D3D12
description: Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in d3dx12.h deklariert.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Hilfsfunktionen
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102134"
---
# <a name="helper-functions-for-d3d12"></a>Funktionen des Hilfsprogramms für D3D12

Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in **d3dx12.h deklariert.**

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | Beschreibung                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](commandlistcast.md)<br/>                                     | Diese Funktionsvorlage wandelt einen konstanten Zeiger auf eine beliebige Befehlsliste in einen const-Zeiger auf eine ID3D12CommandList um.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Berechnet einen Unterressourcenindex für eine Textur. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Gibt den MIP-Slice, den Arrayslice und den Ebenenslice aus, die dem angegebenen Unterressourcenindex entsprechen. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter ab **(id3D12Device**). <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Gibt an, ob das Layout nicht transparent ist.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Gibt den Unterobjekttyp zurück, der der Basisklasse des übergebenen Unterobjekttyps entspricht.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analysiert eine Pipelinezustandsstreambeschreibung und ruft einen benutzerdefinierten Rückruf für jede analysierte Unterobjektinstanz auf.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Unterstützt die Aktivierung von Root Signature 1.1-Features, wenn sie verfügbar sind, und erfordert keine Zwei-Codepfade zum Erstellen von Stammsignaturen. Diese Hilfsmethode rekonstruiert eine Stammsignatur der Version 1.0, wenn Version 1.1 nicht unterstützt wird.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Gibt die erforderliche Größe eines Puffers zurück, der für den Datenupload verwendet werden soll. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Kopiert eine Unterressourcenzeile nach Zeile. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Aktualisiert Unterressourcen. Alle Unterressourcenarrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (heap-allocating)**](updatesubresources2.md)<br/>                    | Aktualisiert Unterressourcen mit einer Heapzuweisungsimplementierung. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (stack-allocating)**](updatesubresources3.md)<br/>                   | Aktualisiert Unterressourcen mit einer Stapelzuweisungsimplementierung. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Strukturen und Funktionen des Hilfsprogramms für D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





