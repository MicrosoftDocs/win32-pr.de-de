---
description: Einführung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Einführung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb61f41644f74e22f8e4117854db90cc1bea025b3ff5399819eaa580eee39f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994920"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Einführung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)

Auf der ganzen Welt übernehmen viele Unternehmen Windows 7 aufgrund ihrer Unternehmensfeatures und -fähigkeiten. IT-Abteilungen ändern auch die Art und Weise, wie sie ihre langfristigen Plattformanforderungen zur Unterstützung eines modernen Desktops erfüllen. Das Windows 7-Betriebssystem trägt dazu bei, die Gesamtkosten zu senken, indem es Benutzern hilft, überall produktiv zu bleiben, die Sicherheit und Kontrolle zu verbessern und die Desktopverwaltung in der gesamten Organisation zu vereinfachen. Windows 7 enthält auch einen standardbasierten modernen Browser, Windows Internet Explorer 8, der verbesserte Sicherheit und erweiterte Browserfunktionen bietet. Diese beiden Plattformen erhöhen die IT-Effizienz und verbessern die Agilität und Sicherheit einer Organisation.

Die Migration zu einem neuen Betriebssystem bringt jedoch besondere Herausforderungen mit sich, in erster Linie mit der Notwendigkeit, ältere Webanwendungen zu unterstützen. Unternehmen verfügen möglicherweise über Anwendungen, die für frühere Versionen von Windows Internet Explorer erstellt wurden, z. B. Windows Internet Explorer 7 oder Microsoft Internet Explorer 6. Bei diesen Webanwendungen können Kompatibilitätsprobleme mit Internet Explorer 8 auftreten. Darüber Internet Explorer 6 nicht nativ unter Windows 7 ausgeführt, und Windows unterstützt nicht die gleichzeitige Ausführung von Internet Explorer Versionen. Weitere Informationen finden Sie im Microsoft Knowledge Base Artikel Ausführen mehrerer Versionen von Internet Explorer unter einem einzelnen Betriebssystem[wird nicht unterstützt."](https://support.microsoft.com/kb/2020599)

Viele Unternehmen verwenden weiterhin Internet Explorer 6-basierten Webanwendungen, die in den letzten zehn Jahren erstellt und angepasst wurden. Unternehmen, die die Bereitstellung von Windows 7 planen, benötigen eine umfassende Strategie und einen Ausführungsplan, um Ältere Webanwendungen zu Internet Explorer 8 zu migrieren. Dieses Dokument bietet eine ausführliche Übersicht über Internet Explorer 8-Kompatibilitätsprobleme, erläutert die Migration von Webanwendungen und stellt verwandte Tools und Prozesse vor.

Das Internet Explorer 8-Release konzentriert sich auf drei Hauptthemen:

-   Stellen Sie in der Realen Interoperabilität mit anderen Browsern und Kompatibilität für vorhandene Websites zur Verfügung.
-   Beschleunigen und vereinfachen Sie die Webentwicklung mithilfe der integrierten Entwicklertools.
-   Ermöglichen Sie Benutzererfahrungen, die über die Seite hinausgehen, über neue Browserfeatures, die Benutzer mit innovativen Webdiensten verbinden.

Zusätzlich zu den erheblichen Fortschritten bei der Unterstützung von Standards enthält Internet Explorer 8 zusätzliche Plattforminvestitionen für Entwickler. Internet Explorer 8 verbessert die Leistung in vielen Internet Explorer-Subsystemen, z. B. dem HTML-Parser, css-Regelverarbeitung (Cascading StyleSheet), Markupstrukturbearbeitung, JavaScript-Parser, Garbage Collector-Runtime und Speicherverwaltung. Weitere Entwicklerinvestitionen umfassen Folgendes:

-   CSS 2.1: Sie können Ihre Seiten einmal schreiben und einfacher in verschiedenen Browsern rendern, da Internet Explorer 8 die CSS 2.1-Spezifikation vollständig unterstützt.
-   Dokumentobjektmodell (DOM) und HTML 4.01: Internet Explorer 8 bietet zusätzliche HTML 4.01-Verbesserungen und vollständige CSS 2.1-Konformität. Internet Explorer 8 behebt auch viele browserübergreifende Inkonsistenzen. Beispielsweise ist die Get/Set/Remove-Attributimplementierung jetzt mit anderen Browsern interoperabel, und die Leistung wird in asynchronen JavaScript- und XML-Entwurfsmustern (AJAX) verbessert.
-   Neue Standards: Internet Explorer 8 umfasst zukünftige Standards, z. B. den HTML5 Draft DOM Storage-Standard von W3C, die SElektor-API der Arbeitsgruppe webanwendungen und die von ECMAScript 3.1 unterstützte Syntax.
-   Neue Navigationsfunktionen für AJAX-Anwendungen: Sie können den Navigationsstapel und die Adressleiste des Browsers von ajax-Anwendungen aktualisieren, damit diese Browserfeatures in Ihrer Anwendung ordnungsgemäß funktionieren.
-   Acid2: Internet Explorer 8 rendert den Acid2-Browsertest ordnungsgemäß.
-   Kompatibilität: Internet Explorer 8 enthält eine standardkompatible Layout-Engine, mit der Sie eine standardbasierte Website für mehrere Browser erstellen können. Um Ihre Websites einfacher zur neuen standardkonformen Layout-Engine zu migrieren, können Sie mit Internet Explorer 8 die Internet Explorer  7-Layout-Engine verwenden, indem Sie ein einfaches Metaelement in Ihren Code einfügen oder einen einzelnen HTTP-Header auf Ihren Servern hinzufügen.
-   Entwicklertools: Entwicklertools in Internet Explorer (auf das Sie durch Drücken der F12-Taste zugreifen), können Sie HTML-, CSS- und JavaScript-Code in einer visuellen Umgebung schnell debuggen. Diese Tools sind direkt in Internet Explorer 8 mit erweiterter Funktionalität enthalten, einschließlich einer Option, mit der Sie auswählen können, welche Anwendung beim Anzeigen der Quelle einer Webseite verwendet werden soll. Sie können Probleme schnell erkennen und beheben, da das Tool umfassende Einblicke in das DOM bietet.
-   Weitere Informationen zu den neuen und erweiterten Features von Internet Explorer 8 finden Sie unter Neues [in Internet Explorer 8 in](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



