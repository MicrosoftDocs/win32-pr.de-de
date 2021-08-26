---
title: MSAA ist nicht für Windows Store verfügbar
description: MSAA ist nicht für Windows Store verfügbar
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabfd0f855cc4d3940a68fd18e69c4ca2a93774ccdbd0fb1868d2f8f489abea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935080"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA ist nicht für Windows Store verfügbar

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

Windows 8 unterstützt msaa (Microsoft Active Accessibility) nicht zum Lesen oder Automatisieren zugänglicher Daten aus Windows Store Apps. Die Benutzeroberflächenautomatisierung-API (UIA), die seit Windows 7 verfügbar ist, sollte stattdessen verwendet werden. Da keine app-Windows Store vorhanden sind, gibt es keine vorhandenen Implementierungen, die von dieser Änderung betroffen sind. Dies wirkt sich nur auf neue Apps und Features aus, die für Windows 8. Entwickler können weiterhin MSAA verwenden, um ihre Barrierefreiheitsdaten verfügbar zu machen. Wenn MSAA-Daten von einem Windows Store bereitgestellt werden, können UIA-Clients die Daten weiterhin lesen und automatisieren.

Um die API für Windows 8Windows Store-Apps zu vereinfachen, haben wir uns entschieden, nur Benutzeroberflächenautomatisierung als Client für diese Apps zu unterstützen. UIA-Clients können UIA-Anbieter ohne Übersetzung nativ lesen. UIA-Clients können MSAA-Anbieter so lesen, wie sie über den UIA-zu-MSAA-Proxy übersetzt werden. Dies reduziert den Testaufwand für Windows Store App-Entwickler.

Die Beseitigung der Unterstützung für MSAA-Anbieter würde die Testmatrix weiter reduzieren, aber es gibt wichtige Apps, die noch MSAA-basiert sind und nicht darauf zugreifen möchten.

## <a name="manifestation"></a>Manifestation

Windows Store App-Entwickler nicht auf die Details der MSAA innerhalb des App-Modells zugreifen können.

## <a name="solution"></a>Lösung

Es sollten keine neuen automatisierten Fälle in MSAA für Features von Windows Store werden.

Wechseln Sie alle vorhandenen integrierten Tools, die MSAA verwenden, zu UIA, wenn sie mit Windows Store interagieren müssen. Windows Store App-Entwickler sollten die Benutzeroberflächenautomatisierung-API verwenden.

## <a name="resources"></a>Ressourcen

-   [Grundlagen der Benutzeroberflächenautomatisierung](../winauto/entry-uiauto-win32.md)

 

 