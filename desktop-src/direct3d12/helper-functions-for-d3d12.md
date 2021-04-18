---
title: Funktionen des Hilfsprogramms für D3D12
description: Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von unter Berichten und werden in d3dx12. h deklariert.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Hilfsfunktionen
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341250"
---
# <a name="helper-functions-for-d3d12"></a>Funktionen des Hilfsprogramms für D3D12

Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von unter Berichten und werden in **d3dx12. h** deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](cd3dx12-shader-bytecode.md)<br/>                                     | Diese Funktions Vorlage wandelt einen Konstanten Zeiger auf eine beliebige Befehlsliste in einen Konstanten Zeiger auf einen ID3D12CommandList um.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Berechnet einen subresource-Index für eine Textur. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Gibt die MIP-Slice, den Array Slice und den Ebenen-Slice aus, die dem angegebenen unter Quell Index entsprechen. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter (ein **ID3D12Device**) ab. <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Gibt an, ob das Layout nicht transparent ist.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Gibt den untergeordneten Objekttyp zurück, der der Basisklasse des übergeordneten untergeordneten Objekts entspricht.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analysiert eine Pipeline Status-Datenstrom Beschreibung und ruft für jede analysierte untergeordnete Instanz einen benutzerdefinierten Rückruf auf.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Unterstützt die Aktivierung von root Signature 1,1-Features, wenn diese verfügbar sind. es ist nicht erforderlich, zwei Codepfade zum Aufbauen von Stamm Signaturen zu verwalten. Diese Hilfsmethode rekonstruiert eine Stamm Signatur der Version 1,0, wenn Version 1,1 nicht unterstützt wird.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Gibt die erforderliche Größe eines Puffers zurück, der zum Hochladen von Daten verwendet werden soll. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Kopiert eine untergeordnete Quelle zeilenweise. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Aktualisiert unter Berichte, alle unter Quell Arrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (heap-allocating)**](updatesubresources2.md)<br/>                    | Aktualisiert unter Ressourcen mit einer Heap Zuweisungs Implementierung. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (stack-allocating)**](updatesubresources3.md)<br/>                   | Aktualisiert unter Ressourcen mit einer Implementierung zur Stapel Zuweisung. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Strukturen und Funktionen des Hilfsprogramms für D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





