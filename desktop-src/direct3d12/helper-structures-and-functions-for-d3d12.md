---
title: Hilfsstrukturen und -funktionen für Direct3D 12
description: Diese Hilfsstrukturen und Hilfsfunktionen werden in `d3dx12.h` deklariert.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Hilfsfunktionen
- Hilfsstrukturen
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b42bc9ae73f3537cc786a465feba596b3392401
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812181"
---
# <a name="helper-structures-and-functions-for-direct3d-12"></a>Hilfsstrukturen und -funktionen für Direct3D 12

Diese Hilfsstrukturen und Hilfsfunktionen werden in `d3dx12.h` deklariert.

`d3dx12.h` ist getrennt von den Direct3D 12-Headern verfügbar. Sie können `d3dx12.h` von [der D3D12-Hilfsbibliothek](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)herunterladen.

Sie können diese Hilfsstrukturen verwenden, um Direct3D-Strukturen zu erstellen und zu initialisieren. Diese Hilfsstrukturen verhalten sich wie C++-Klassen. Jede Hilfsstruktur verfügt in der Regel über einen Standardkonstruktor, einen expliziten Konstruktor, einen Destruktor und einen Umwandlungsoperator für die zugeordnete D3D12-Struktur. Jede Hilfsstruktur verfügt über ein C-Präfix und ist einer D3D12-Struktur zugeordnet, der das Präfix "C" fehlt. Die meisten Hilfsstrukturen enthalten Initialisierungsmembermethoden, einige enthalten Vergleichsfunktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Schnittstellen des Hilfsprogramms für D3D12](helper-interfaces-for-d3d12.md) | Diese Hilfsschnittstellen helfen insbesondere bei der Verarbeitung von Unterressourcen und werden in `d3dx12.h` deklariert.  |
| [Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md) | Diese Hilfsstrukturen helfen bei der Initialisierung vieler Direct3D 12-Strukturen und werden in `d3dx12.h` deklariert. |
| [Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md) | Diese Hilfsfunktionen helfen insbesondere bei der Behandlung von Unterressourcen und werden in `d3dx12.h` deklariert.  |

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz für Direct3D 12](direct3d-12-reference.md)
