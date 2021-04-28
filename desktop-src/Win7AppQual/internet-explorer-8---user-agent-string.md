---
description: 'Internet Explorer 8: Benutzer-Agent-Zeichenfolge'
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: 'Internet Explorer 8: Benutzer-Agent-Zeichenfolge'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088238"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8: Benutzer-Agent-Zeichenfolge

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkung von Features

**Schweregrad:** Mittel  
**Häufigkeit** – Hoch  











## <a name="description"></a>BESCHREIBUNG

Die Benutzer-Agent-Zeichenfolge ist Internet Explorer Bezeichner, der Daten zu seiner Version und anderen Attributen für Webserver zur Verfügung stellt. Viele Webanwendungen basieren auf und piggyback auf der Zeichenfolge des IE-Benutzer-Agents. Solche, die dies tun und von einer früheren Versionsnummer abhängen, sind davon abhängig. Die Benutzer-Agent-Zeichenfolge enthält jetzt die Zeichenfolge "Trident/4.0", um die Unterscheidung zwischen der Internet Explorer 7-Benutzer-Agent-Zeichenfolge und der Internet Explorer 8-Benutzer-Agent-Zeichenfolge zu ermöglichen, wenn sie in Internet Explorer 7 Kompatibilitätsansicht. Weitere Informationen finden Sie unter Grundlegendes zu Benutzer-Agent-Zeichenfolgen.

## <a name="manifestation-of-impact"></a>Auswirkungen

Es gibt zwei bereiche, die sich auf diese Auswirken auswirken:

-   Webseiten, die die Benutzer-Agent-Zeichenfolge explizit überprüfen und die Internet Explorer 8-Benutzer-Agent-Zeichenfolge nicht unterstützen, werden möglicherweise nicht ordnungsgemäß ausgeführt. In den meisten Fällen bedeutet dies, dass die Seiten Benutzern den Inhalt blockieren, auf den sie zugreifen oder falsche oder falsch formatierte Inhalte anzeigen.
-   Anwendungen, die Trident hosten (siehe Hosting und Wiederverwendung), verwenden standardmäßig Internet Explorer 7 mit der optionalen Webkomponente, haben jedoch keinen Zugriff auf Internet Explorer 8-Features.

## <a name="solution"></a>Lösung

Stellen Sie sicher, dass Ihre Anwendungen die neue MSIE 8.0-Version in der Benutzer-Agent-Zeichenfolge ordnungsgemäß verarbeiten. Sie können auch die Internet Explorer 7-Kompatibilitätsansicht für diese Anwendungen basierend auf Internet Explorer 7 wählen. Dies kann mit Metatags erfolgen. Weitere Informationen finden Sie in der Erläuterung unter Grundlegendes zu Benutzer-Agent-Zeichenfolgen.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

-   Führen Sie Ihre Anwendungen und Webseiten in einer Internet Explorer 8-Umgebung unter Windows Vista oder Windows XP aus, um sicherzustellen, dass sie sich auf die gewünschte Weise verhalten.
-   Alternativ können Sie das mit dem Application Compatibility Toolkit (ACT) bereitgestellte Internet Explorer Compatibility Test Tool (IECTT) ausführen, um mögliche Probleme aufgrund von Sicherheitsupdates zu finden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Grundlegendes zu Benutzer-Agent-Zeichenfolgen](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Internet Explorer 8 User-Agent Zeichenfolge](/archive/blogs/ie/)
-   [Benutzer-Agent-Zeichenfolge und Versionsvektor](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hosting und Wiederverwendung](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Herunterladen des Anwendungskompatibilitätstoolkits](/windows-hardware/get-started/adk-install)
-   [Bekannte probleme mit Internet Explorer-Sicherheitsfeatures](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
