---
description: .
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Einführung (Cookbook für Windows 7 und Windows Server 2008 R2 Anwendungsqualität)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d491802735ddf1ef75a7a183cd49afea2cc657b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362299"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Einführung (Cookbook für Windows 7 und Windows Server 2008 R2 Anwendungsqualität)

Auf der ganzen Welt nehmen viele Unternehmen aufgrund der Unternehmens Features und-Fähigkeiten Windows 7 in Betrieb. IT-Abteilungen verändern auch, wie Sie Ihren langfristigen Platt Form Anforderungen zur Unterstützung eines modernen Desktops nähern. Mit dem Betriebssystem Windows 7 können Sie die Gesamtbetriebskosten senken, indem Sie den Benutzern dabei helfen, produktiv zu bleiben, die Sicherheit und Kontrolle zu erhöhen und die Desktop Verwaltung im gesamten Unternehmen zu vereinfachen. Windows 7 umfasst auch einen Standard basierten modernen Browser, Windows Internet Explorer 8, der verbesserte Sicherheit und verbesserte Browserfunktionen bietet. Diese beiden Plattformen steigern die IT-Effizienz und verbessern die Agilität und Sicherheit einer Organisation.

Die Migration zu einem neuen Betriebssystem führt jedoch zu besonderen Herausforderungen, in erster Linie mit der Notwendigkeit, ältere Webanwendungen zu unterstützen. Unternehmen verfügen möglicherweise über Anwendungen, die für frühere Versionen von Windows Internet Explorer erstellt wurden, z. b. Windows Internet Explorer 7 oder Microsoft Internet Explorer 6. Diese Webanwendungen können Kompatibilitätsprobleme mit Internet Explorer 8 haben. Außerdem wird Internet Explorer 6 nicht nativ unter Windows 7 ausgeführt, und Windows bietet keine Unterstützung für die gleichzeitige Ausführung von zwei Versionen von Internet Explorer. Weitere Informationen finden Sie im Microsoft Knowledge Base-Artikel "[Ausführen mehrerer Versionen von Internet Explorer auf einem einzelnen Betriebs System wird nicht unterstützt](https://support.microsoft.com/kb/2020599)".

Viele Unternehmen verwenden weiterhin Internet Explorer 6-basierte Webanwendungen, die im Laufe des letzten Jahrzehnts erstellt und angepasst wurden. Unternehmen, die die Bereitstellung von Windows 7 planen, benötigen eine umfassende Strategie und einen Ausführungsplan, um Legacy-Webanwendungen zu Internet Explorer 8 zu migrieren. Dieses Dokument enthält eine ausführliche Übersicht über Kompatibilitätsprobleme mit Internet Explorer 8, erläutert, wie Webanwendungen migriert werden, und stellt verwandte Tools und Prozesse vor.

Die Internet Explorer 8-Version konzentriert sich auf drei wichtige Themen:

-   Sorgen Sie für eine reale Interoperabilität mit anderen Browsern und Kompatibilität für vorhandene Websites.
-   Mithilfe der integrierten Entwicklertools können Sie die Webentwicklung schneller und einfacher gestalten.
-   Aktivieren Sie Oberflächen, die über die Seite hinausgehen, über neue Browser Features, die Benutzer mit innovativen Webdiensten verbinden.

Zusätzlich zu erheblichen Fortschritten bei der Standardunterstützung enthält Internet Explorer 8 zusätzliche Platt Form Investitionen für Entwickler. Internet Explorer 8 verbessert die Leistung in vielen Internet Explorer-Subsystemen, wie z. b. der HTML-Parser, Cascading Stylesheet (CSS)-Regelverarbeitung, Markup Struktur Bearbeitung, Javascript-Parser, Garbage Collector-Laufzeit und Speicherverwaltung. Weitere Entwickler Investitionen sind:

-   CSS 2,1: Sie können Ihre Seiten einmal schreiben und leichter in verschiedenen Browsern ordnungsgemäß Rendering haben, da Internet Explorer 8 die CSS 2,1-Spezifikation vollständig unterstützt.
-   Dokumentobjektmodell (DOM) und HTML 4,01-Verbesserungen: Internet Explorer 8 bietet zusätzliche HTML 4,01-Verbesserungen und vollständige CSS 2,1-Konformität. Internet Explorer 8 korrigiert außerdem viele Browser übergreifende Inkonsistenzen. Beispielsweise ist die Get/Set/Remove-Attribut Implementierung nun mit anderen Browsern interoperabel, und die Leistung wird in den Entwurfsmustern asynchronen JavaScript und XML (Ajax) verbessert.
-   Neue Standards: Internet Explorer 8 umfasst zukünftige Standards, z. b. den W3C HTML5-Entwurfs-DOM Storage Standard, die Selectors-API der Arbeitsgruppe der Webanwendungen und die unterstützte ECMAScript 3,1-Syntax.
-   Neue Navigations Features für AJAX-Anwendungen: Sie können den Browser-und vorwärts Navigations Stapel und die Adressleiste von AJAX-Anwendungen aus aktualisieren, damit diese Browserfunktionen in Ihrer Anwendung ordnungsgemäß funktionieren.
-   Acid2: Internet Explorer 8 rendert den Acid2-Browser Test ordnungsgemäß.
-   Kompatibilität: Internet Explorer 8 enthält eine besser kompatible LayoutEngine, mit der Sie eine Standard basierte Site für mehrere Browser erstellen können. Zum einfacheren Migrieren Ihrer Websites zum neuen Standard kompatiblen Layoutmodul ermöglicht Internet Explorer 8 die Verwendung des Layout-Moduls von Internet Explorer 7, indem Sie ein einfaches **Meta** -Element in den Code einfügen oder einen einzelnen HTTP-Header auf den Servern hinzufügen.
-   Entwicklertools: Entwicklertools in Internet Explorer (durch Drücken der Taste F12) können Sie schnell HTML-, CSS-und JavaScript-Code in einer visuellen Umgebung debuggen. Diese Tools sind direkt in Internet Explorer 8 mit erweiterter Funktionalität enthalten, einschließlich der Option Ann, um auszuwählen, welche Anwendung beim Anzeigen der Quelle einer Webseite verwendet werden soll. Sie können Probleme schnell erkennen und beheben, indem Sie die umfassenden Einblicke des Tools im Dom erhalten.
-   Weitere Informationen zu den neuen und verbesserten Features von Internet Explorer 8 finden Sie unter [What es New in Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



