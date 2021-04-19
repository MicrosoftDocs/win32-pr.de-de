---
title: Hohe dpi-Informationen für Desktop-Apps in Windows 8.1
description: Hohe dpi-Informationen für Desktop-Apps in Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341732"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Hohe dpi-Informationen für Desktop-Apps in Windows 8.1

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

In Windows 8.1 die Windows-Desktop Anwendungen zusätzlich zu den in Windows 8 unterstützten Skalierungen 200 von 100%, 125% und 150% ausgeführt werden. Außerdem werden Desktop Anwendungen pro Monitor skaliert und nicht in einem einzelnen Skalierungsfaktor, der auf alle anzeigen angewendet wird. Entwickler können auch neue APIs in Windows 8.1 anrufen, um Skalierungsfaktoren pro Monitor zu erhalten.

## <a name="manifestations"></a>Kundgebungen

Benutzer können neue High Density-Anzeige mit Windows 8.1 für eine fantastische visuelle Darstellung verwenden, die die höheren Pixeldaten nutzt. Wenn Anwendungen keine hohen DPI-Werte verarbeiten, werden Sie von Windows für den Benutzer skaliert. Außerdem können Benutzer eine Mischung aus hoher und niedriger Dichte auf demselben Computer verwenden, und Windows skaliert Inhalt für jede Anzeige entsprechend. Dies ist eine Verbesserung gegenüber Windows 8, bei der Inhalte für einige anzeigen zu groß sein können.

## <a name="mitigation"></a>Minderung

Da Windows apps skaliert, die sich nicht selbst skalieren lassen, müssen Entwickler in der Regel keine zusätzlichen Aufgaben erledigen, aber Entwickler, die in das Schreiben von Anwendungen investieren, die High dpi unterstützen, haben einen Wettbewerbsvorteil, da diese Anwendungen auf neuen Hochleistungs-Laptops und Desktop Monitoren besser aussehen werden.

## <a name="solution"></a>Lösung

Eine Anwendung, die hohe dpi-Schritte nutzen kann, ist eine komplexe Entwurfs-und Implementierungs Aufgabe. Unter den Links unten finden Sie Lernprogramm Informationen, Inhalte der buildpräsentation und ähnliche Unterstützung.

## <a name="tests"></a>Tests

Selbst wenn Entwickler ihre Anwendungen nicht für hohe dpi-Vorgänge nutzen, sollten Sie Ihre Anwendung bei 100%, 125%, 150% und der Skalierung von 200% testen, um sicherzustellen, dass die Endbenutzer Leistung zufriedenstellend und wettbewerbsfähig ist.

## <a name="resources"></a>Ressourcen

-   [Whitepaper und Tutorial zu hohen dpi-Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Windows-Desktop-Beispiel Programme](https://www.microsoft.com/?ref=go)
-   [Build 2013-Break-out-Sitzung mit hoher dpi in Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 