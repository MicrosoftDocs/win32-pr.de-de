---
title: Strukturen und Funktionen des Hilfsprogramms für D3D12
description: Diese Hilfsstrukturen und Hilfsfunktionen werden in d3dx12. h deklariert.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Hilfsfunktionen
- Hilfsstrukturen
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341249"
---
# <a name="helper-structures-and-functions-for-d3d12"></a>Strukturen und Funktionen des Hilfsprogramms für D3D12

Diese Hilfsstrukturen und Hilfsfunktionen werden in **d3dx12. h** deklariert.

Sie können diese Hilfsstrukturen verwenden, um Direct3D-Strukturen zu erstellen und zu initialisieren. Diese Hilfsstrukturen Verhalten sich wie C++-Klassen. Jede hilfsstruktur verfügt in der Regel über einen Standardkonstruktor, einen expliziten Konstruktor, einen destrukturtor und einen Cast Operator für die zugeordnete D3D12-Struktur. Jede hilfsstruktur verfügt über ein Präfix "c" und ist mit einer D3D12-Struktur verknüpft, der das Präfix "c" fehlt. Die meisten Hilfsstrukturen enthalten Methoden für Initialisierungs Member, von denen einige Vergleichsfunktionen enthalten.

**d3dx12. h** ist separat von den Direct3D 12-Headern verfügbar. Sie können **d3dx12. h** von [der D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12)herunterladen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Schnittstellen des Hilfsprogramms für D3D12](helper-interfaces-for-d3d12.md)<br/> | Diese hilfsschnittstellen helfen insbesondere bei der Behandlung von unter Berichten und werden in **d3dx12. h** deklariert. <br/>        |
| [Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)<br/> | Diese Hilfsstrukturen helfen dabei, viele der Direct3D 12-Strukturen zu initialisieren, und werden in **d3dx12. h** deklariert.<br/> |
| [Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)<br/>   | Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von unter Berichten und werden in **d3dx12. h** deklariert. <br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





