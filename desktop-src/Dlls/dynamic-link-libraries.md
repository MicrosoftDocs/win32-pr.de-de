---
description: Eine Dynamic Link Library (dll) ist ein Modul, das Funktionen und Daten enthält, die von einem anderen Modul (Anwendung oder dll) verwendet werden können.
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Dynamic-Link-Bibliotheken (Dynamic Link Libraries)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753784"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Dynamic-Link-Bibliotheken (Dynamic Link Libraries)

Eine *Dynamic Link Library* (dll) ist ein Modul, das Funktionen und Daten enthält, die von einem anderen Modul (Anwendung oder dll) verwendet werden können.

Eine DLL kann zwei Arten von Funktionen definieren: "exportiert" und "intern". Die exportierten Funktionen sind für das Aufrufen durch andere Module sowie für das Aufrufen in der dll vorgesehen, in der Sie definiert sind. Interne Funktionen sollten in der Regel nur innerhalb der dll aufgerufen werden, in der Sie definiert sind. Obwohl eine DLL Daten exportieren kann, werden Ihre Daten im Allgemeinen nur von ihren Funktionen verwendet. Es ist jedoch nichts zu verhindern, dass ein anderes Modul diese Adresse liest oder schreibt.

DLLs bieten eine Möglichkeit, Anwendungen zu modularisieren, damit ihre Funktionalität leichter aktualisiert und wieder verwendet werden kann. DLLs helfen auch, den Arbeitsspeicher Aufwand zu reduzieren, wenn mehrere Anwendungen gleichzeitig dieselbe Funktionalität verwenden, denn obwohl jede Anwendung eine eigene Kopie der DLL-Daten erhält, verwenden die Anwendungen den DLL-Code gemeinsam.

Die Windows-Anwendungsprogrammierschnittstelle (API) ist als ein Satz von DLLs implementiert, sodass jeder Prozess, der die Windows-API verwendet, dynamisches Verknüpfen verwendet.

-   [Informationen zu Dynamic-Link-Bibliotheken](about-dynamic-link-libraries.md)
-   [Verwenden von Dynamic-Link-Bibliotheken](using-dynamic-link-libraries.md)
-   [Dynamic Link Library-Referenz](dynamic-link-library-reference.md)

> [!Note]  
> Wenn ein Benutzer Probleme mit einer DLL auf Ihrem Computer hat, wenden Sie sich an den Kundensupport des Softwareanbieters, der die dll veröffentlicht. Wenn Sie der Meinung sind, dass Sie Unterstützung für ein Microsoft-Produkt (einschließlich Windows) benötigen, besuchen Sie unsere technische Support Website unter [Support.Microsoft.com](https://support.microsoft.com).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
