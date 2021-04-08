---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-Benutzer-Agent-Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be481cf409468d9d182d37ae7636b167bc71d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865971"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8-Benutzer-Agent-Zeichenfolge

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** -Windows XP \| Windows Vista \| Windows 7  
**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Häufigkeit** -hoch  











## <a name="description"></a>BESCHREIBUNG

Die Benutzer-Agent-Zeichenfolge ist der Internet Explorer-Bezeichner, der Daten über seine Version und andere Attribute für Webserver bereitstellt. Viele Webanwendungen verlassen sich auf die Benutzer-Agent-Zeichenfolge des IE-Benutzers und greifen darauf zurück. Solche, die dies tun und von einer früheren Versionsnummer abhängen, sind betroffen. Die Zeichenfolge des Benutzer-Agents enthält nun die Zeichenfolge "dreident/4.0", um Unterschiede zwischen der Benutzer-Agent-Zeichenfolge von Internet Explorer 7 und der Zeichenfolge des Benutzer-Agents von Internet Explorer 8 bei Ausführung in der Kompatibilitäts Ansicht von Internet Explorer 7 Weitere Informationen finden Sie Untergrund Legendes zu Benutzer-Agent

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Es gibt zwei betroffene Bereiche:

-   Webseiten, die die Benutzer-Agent-Zeichenfolge explizit überprüfen und die Benutzer-Agent-Zeichenfolge von Internet Explorer 8 nicht unterstützen, werden möglicherweise nicht In den meisten Fällen bedeutet dies, dass die Seiten Benutzer aus dem Inhalt blockieren, auf den Sie zugreifen möchten, oder dass falsche oder falsch formatierte Inhalte angezeigt werden.
-   Anwendungen, die einen Einzug hosten (siehe Hosting und Wiederverwendung), werden standardmäßig Internet Explorer 7 verwendet, wobei die optionale Webkomponente verwendet wird. Sie haben jedoch keinen Zugriff auf Internet Explorer 8-Funktionen.

## <a name="solution"></a>Lösung

Stellen Sie sicher, dass die Anwendung die neue Version "MSIE 8,0" in der Zeichenfolge des Benutzer-Agents ordnungsgemäß verarbeitet. Sie können auch die Kompatibilitäts Ansicht von Internet Explorer 7 für Anwendungen, die auf Internet Explorer 7 basieren, anmelden. Dies kann mit Meta-Tags erfolgen. Weitere Informationen finden Sie Untergrund Legendes zu Benutzer-Agent-Zeichen folgen.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

-   Führen Sie Ihre Anwendungen und Webseiten in einer Internet Explorer 8-Umgebung unter Windows Vista oder Windows XP aus, um sicherzustellen, dass Sie sich auf die gewünschte Weise Verhalten.
-   Alternativ können Sie das mit dem Anwendungskompatibilitäts-Toolkit (Application Compatibility Toolkit, Act) bereitgestellte Internet Explorer Compatibility Test Tool (iectt) ausführen, um mögliche Probleme aufgrund von Updates der Sicherheitsfeatures zu ermitteln.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Grundlegendes zu Benutzer-Agent](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Internet Explorer 8-User-Agent Zeichenfolge](/archive/blogs/ie/)
-   [Benutzer-Agent-Zeichenfolge und Versions Vektor](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hosting und Wiederverwendung](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Anwendungskompatibilitäts-Toolkit Download](/windows-hardware/get-started/adk-install)
-   [Bekannte Probleme mit der Internet Explorer-Sicherheitsfunktion](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
