---
description: Einführung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Einführung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4125c2bd122d239c155f089f06bef2f455ee121b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088198"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Einführung (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)

Auf der ganzen Welt übernehmen viele Unternehmen Windows 7 aufgrund seiner Unternehmensfeatures und -fähigkeiten. IT-Abteilungen ändern auch, wie sie ihre langfristigen Plattformanforderungen zur Unterstützung eines modernen Desktops angehen. Das Windows 7-Betriebssystem trägt dazu bei, die Gesamtkosten zu senken, indem es Benutzern hilft, überall produktiv zu bleiben, die Sicherheit und Kontrolle zu verbessern und die Desktopverwaltung in der gesamten Organisation zu vereinfachen. Windows 7 enthält auch einen standardbasierten modernen Browser, Windows Internet Explorer 8, der verbesserte Sicherheit und erweiterte Browserfunktionen bietet. Diese beiden Plattformen steigern die IT-Effizienz und verbessern die Agilität und Sicherheit einer Organisation.

Die Migration zu einem neuen Betriebssystem führt jedoch zu besonderen Herausforderungen, in erster Linie mit der Notwendigkeit, Ältere Webanwendungen zu unterstützen. Unternehmen verfügen möglicherweise über Anwendungen, die für frühere Versionen von Windows Internet Explorer erstellt wurden, z. B. Windows Internet Explorer 7 oder Microsoft Internet Explorer 6. Bei diesen Webanwendungen können Kompatibilitätsprobleme mit Internet Explorer 8 auftreten. Darüber hinaus wird Internet Explorer 6 nicht nativ unter Windows 7 ausgeführt, und Windows unterstützt nicht die gleichzeitige Ausführung von zwei Versionen von Internet Explorer. Weitere Informationen finden Sie im Microsoft Knowledge Base Artikel["Ausführen mehrerer Versionen von Internet Explorer unter einem einzelnen Betriebssystem wird nicht unterstützt."](https://support.microsoft.com/kb/2020599)

Viele Unternehmen verwenden weiterhin Internet Explorer 6-basierte Webanwendungen, die in den letzten zehn Jahren erstellt und angepasst wurden. Unternehmen, die Windows 7 bereitstellen möchten, benötigen eine umfassende Strategie und einen Ausführungsplan, um Legacywebanwendungen zu Internet Explorer 8 zu migrieren. Dieses Dokument bietet eine ausführliche Übersicht über Internet Explorer 8-Kompatibilitätsprobleme, erläutert die Migration von Webanwendungen und stellt verwandte Tools und Prozesse vor.

Das Internet Explorer 8-Release konzentriert sich auf drei Hauptthemen:

-   Bereitstellen realer Interoperabilität mit anderen Browsern und Kompatibilität für vorhandene Websites.
-   Beschleunigen und vereinfachen Sie die Webentwicklung mithilfe der integrierten Entwicklertools.
-   Ermöglichen Sie Benutzererfahrungen, die über die Seite hinausgehen, durch neue Browserfeatures, die Benutzer mit innovativen Webdiensten verbinden.

Neben erheblichen Fortschritten bei der Unterstützung von Standards enthält Internet Explorer 8 zusätzliche Plattforminvestitionen für Entwickler. Internet Explorer 8 verbessert die Leistung in vielen Internet Explorer-Subsystemen, z. B. dem HTML-Parser, css-Regelverarbeitung (Cascading Stylesheet), Markupstrukturbearbeitung, JavaScript-Parser, Garbage Collector-Runtime und Speicherverwaltung. Weitere Entwicklerinvestitionen umfassen Folgendes:

-   CSS 2.1: Sie können Ihre Seiten einmal schreiben und sie leichter in verschiedenen Browsern ordnungsgemäß rendern lassen, da Internet Explorer 8 die CSS 2.1-Spezifikation vollständig unterstützt.
-   Dokumentobjektmodell (DOM) und HTML 4.01: Internet Explorer 8 bietet zusätzliche HTML 4.01-Verbesserungen und vollständige CSS 2.1-Konformität. Internet Explorer 8 behebt auch viele browserübergreifende Inkonsistenzen. Beispielsweise ist die Get/Set/Remove-Attributimplementierung jetzt mit anderen Browsern interoperabel, und die Leistung wird in asynchronen JavaScript- und XML-Entwurfsmustern (AJAX) verbessert.
-   Neue Standards: Internet Explorer 8 umfasst zukünftige Standards wie den HTML5 Draft DOM Storage-Standard von W3C, die Selektor-API der Arbeitsgruppe webanwendungen und die von ECMAScript 3.1 unterstützte Syntax.
-   Neue Navigationsfunktionen für AJAX-Anwendungen: Sie können den Navigationsstapel und die Adressleiste des Browsers von ajax-Anwendungen aktualisieren, damit diese Browserfeatures in Ihrer Anwendung ordnungsgemäß funktionieren.
-   Acid2: Internet Explorer 8 rendert den Acid2-Browsertest ordnungsgemäß.
-   Kompatibilität: Internet Explorer 8 enthält eine mehr standardkompatible Layout-Engine, mit der Sie eine standardbasierte Website für mehrere Browser erstellen können. Um Ihre Standorte einfacher zur neuen standardkonformen Layout-Engine zu migrieren, können Sie Internet Explorer 8 die Internet Explorer 7-Layout-Engine verwenden, indem Sie ein einfaches **Metaelement** in Ihren Code einfügen oder einen einzelnen HTTP-Header auf Ihren Servern hinzufügen.
-   Entwicklertools: Entwicklertools in Internet Explorer (auf die Sie durch Drücken der F12-Taste zugreifen) ermöglichen ihnen das schnelle Debuggen von HTML-, CSS- und JavaScript-Code in einer visuellen Umgebung. Diese Tools sind direkt in Internet Explorer 8 mit erweiterter Funktionalität enthalten, einschließlich einer Option zum Auswählen der Zu verwendenden Anwendung, wenn Sie die Quelle einer Webseite anzeigen. Aufgrund der umfassenden Einblicke, die das Tool im DOM bietet, können Sie Probleme schnell identifizieren und beheben.
-   Weitere Informationen zu den neuen und erweiterten Features von Internet Explorer 8 finden Sie unter [Neuerungen in Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Adressierung der Anwendungskompatibilität beim Migrieren zu Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



