---
title: Hohe DPI für Desktop-Apps in Windows 8.1
description: Hohe DPI für Desktop-Apps in Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbef80ce11de41ca50b7cf5ce4076b294b9331b62be417686f7ba0a3a63b98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852426"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Hohe DPI für Desktop-Apps in Windows 8.1

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Beschreibung

In Windows 8.1 desktop applications expected to run on displays with 200% scaling addition to the 100%, 125% and 150% scaling that is supported in Windows 8. Darüber hinaus werden Desktopanwendungen auf Monitorbasis skaliert und nicht auf einen einzelnen Skalierungsfaktor, der auf alle Anzeigen angewendet wird. Entwickler können auch neue APIs in Windows 8.1, um Skalierungsfaktoren pro Monitor zu erhalten.

## <a name="manifestations"></a>Manifestationen

Benutzer können neue Displays mit hoher Dichte mit Windows 8.1 für eine hervorragende visuelle Darstellung verwenden, die die höheren Pixeldaten nutzt. Wenn Anwendungen keine hohen DPI-Daten verarbeiten, Windows sie für den Benutzer skalieren. Darüber hinaus können Benutzer eine Mischung aus Displays mit hoher und niedriger Dichte auf demselben Computer verwenden, und Windows Inhalte für jede Anzeige entsprechend skalieren. Dies ist eine Verbesserung gegenüber Windows 8, bei der der Inhalt auf einigen Displays zu groß sein kann.

## <a name="mitigation"></a>Minderung

Da Windows Apps skalieren wird, die nicht selbst skaliert werden, müssen Entwickler in der Regel keine zusätzlichen Arbeiten mehr tun, aber Entwickler, die in das Schreiben von Anwendungen investieren, die eine hohe DPI-Leistung unterstützen, haben einen Wettbewerbsvorteil, da diese Anwendungen auf neuen Laptops und Desktopmonitoren mit hohem DPI-Grad besser aussehen.

## <a name="solution"></a>Lösung

Das Erstellen einer Anwendung, die eine hohe DPI-Leistung nutzen kann, ist eine komplexe Entwurfs- und Implementierungsaufgabe. Unter den unten angegebenen Links finden Sie Tutorialinformationen, Buildpräsentationsinhalte und ähnliche Unterstützung.

## <a name="tests"></a>Tests

Selbst wenn Entwickler sich nicht dafür entscheiden, ihre Anwendungen von einem hohen DPI-Grad zu profitieren, sollten sie ihre Anwendung mit 100 %, 125 %, 150 % und 200 % Skalierung testen, um sicherzustellen, dass die Endbenutzererfahrung zufriedenstellend und wettbewerbsfähig ist.

## <a name="resources"></a>Ressourcen

-   [Whitepaper und Tutorial zu hohen DPI-Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Windows Desktop-Beispielprogrammen](https://www.microsoft.com/?ref=go)
-   [BUILD 2013-Break-Out-Sitzung mit hohem DPI-Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 