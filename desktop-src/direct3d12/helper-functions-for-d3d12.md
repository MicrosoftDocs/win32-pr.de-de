---
title: Hilfsfunktionen für Direct3D 12
description: Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in `d3dx12.h` deklariert.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Hilfsfunktionen
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813189"
---
# <a name="helper-functions-for-direct3d-12"></a>Hilfsfunktionen für Direct3D 12

Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in `d3dx12.h` deklariert.

`d3dx12.h` ist getrennt von den Direct3D 12-Headern verfügbar. Sie können `d3dx12.h` von [der D3D12-Hilfsbibliothek](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)herunterladen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**CommandListCast**](commandlistcast.md) | Diese Funktionsvorlage umgewandelt einen konstanten Zeiger auf eine beliebige Befehlsliste in einen const-Zeiger auf eine ID3D12CommandList. |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | Berechnet einen Unterressourcenindex für eine Textur. |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | Gibt den MIP-Slice, den Arrayslice und den Ebenenslice aus, die dem angegebenen Unterressourcenindex entsprechen. |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | Ruft die Anzahl der Ebenen für das angegebene DXGI-Format für den angegebenen virtuellen Adapter **(ID3D12Device)** ab. |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | Gibt an, ob das Layout nicht transparent ist. |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | Gibt den Unterobjekttyp zurück, der der Basisklasse des übergebenen Unterobjekttyps entspricht. |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | Analysiert eine Beschreibung des Pipelinezustandsstreams und ruft einen benutzerdefinierten Rückruf für jede analysierte Unterobjektinstanz auf. |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | Unterstützt die Aktivierung von Stammsignatur 1.1-Features, wenn diese verfügbar sind, und erfordert keine Verwaltung von zwei Codepfaden zum Erstellen von Stammsignaturen. Diese Hilfsmethode rekonstruiert eine Stammsignatur der Version 1.0, wenn Version 1.1 nicht unterstützt wird. |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | Gibt die erforderliche Größe eines Puffers zurück, der für den Datenupload verwendet werden soll. |
| [**Memcpysubresource**](memcpysubresource.md) | Kopiert eine Unterressource zeile für Zeile. |
| [**Updatesubresources**](updatesubresources1.md) | Aktualisiert Unterressourcen. Alle Unterressourcenarrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device::GetCopyableFootprints.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) |
| [**Updatesubresources (heap-allocating)**](updatesubresources2.md) | Aktualisiert Unterressourcen mit einer Heapzuweisungsimplementierung. |
| [**Updatesubresources (stack-allocating)**](updatesubresources3.md) | Aktualisiert Unterressourcen mit einer Stapelzuweisungsimplementierung. |

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz für Direct3D 12](direct3d-12-reference.md)
* [Strukturen und Funktionen des Hilfsprogramms für D3D12](helper-structures-and-functions-for-d3d12.md)
