---
title: MSAA ist für Windows Store-Apps nicht verfügbar.
description: MSAA ist für Windows Store-Apps nicht verfügbar.
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039743"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA ist für Windows Store-Apps nicht verfügbar.

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

Windows 8 bietet keine Unterstützung für MSAA (Microsoft Active Accessibility) zum Lesen oder Automatisieren von verfügbaren Daten aus Windows Store-Apps. Die UIA-API (UI Automation), die seit Windows 7 verfügbar ist, sollte stattdessen verwendet werden. Da keine Windows Store-App-Features vorhanden sind, sind keine Implementierungen vorhanden, die von dieser Änderung betroffen sind. Dies wirkt sich nur auf neue apps und Features aus, die für Windows 8 geschrieben wurden. Entwickler können weiterhin MSAA verwenden, um Ihre Barrierefreiheits Daten verfügbar zu machen. Wenn MSAA-Daten vom Windows Store-App-Anbieter bereitgestellt werden, sind UIA-Clients weiterhin in der Lage, die Daten zu lesen und zu automatisieren.

Um die API für Windows 8-Windows Store-Apps zu vereinfachen, haben wir entschieden, nur die Automatisierung der Benutzeroberfläche als Client für diese apps zu unterstützen. UIA-Clients können UIA-Anbieter ohne Übersetzung nativ lesen. UIA-Clients können MSAA-Anbieter so lesen, dass Sie über den UIA-zu-MSAA-Proxy übersetzt werden. Dadurch wird die Test Last für Windows Store-App-Entwickler reduziert.

Wenn Sie die Unterstützung für MSAA-Anbieter eliminieren, wird die Test Matrix weiter reduziert, aber es gibt wichtige apps, die weiterhin auf einem MSAA basieren und nicht auf Sie zugreifen möchten.

## <a name="manifestation"></a>Ausstrahlung

Entwickler von Windows Store-Apps sind nicht in der Lage, auf die Details von MSAA innerhalb des App-Modells zuzugreifen.

## <a name="solution"></a>Lösung

In MSAA sollten für Features von Windows Store-Apps keine neuen automatisierten Fälle erstellt werden.

Wechseln Sie alle vorhandenen in-Box-Tools, die MSAA verwenden, zu UIA, wenn Sie mit Windows Store-Apps interagieren müssen. Entwickler von Windows Store-Apps sollten die Benutzeroberflächenautomatisierungs-API verwenden.

## <a name="resources"></a>Ressourcen

-   [Grundlagen der Benutzeroberflächenautomatisierung](../winauto/entry-uiauto-win32.md)

 

 