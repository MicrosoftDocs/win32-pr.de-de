---
description: Dieses Thema bietet einen konzeptionellen Überblick über die technologie mehrsprachige Benutzeroberfläche (USERNAME), die Plattformunterstützung, die sie für die Aktivierung mehrsprachiger Benutzeroberflächen bietet, und die Vorteile, die sie für das Windows Ökosystem bietet.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Übersicht über DIE ÜBERSICHT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e4e92c9103b27b35be427a74174c644a285266
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625776"
---
# <a name="overview-of-mui"></a>Übersicht über DIE ÜBERSICHT

Dieses Thema bietet einen konzeptionellen Überblick über die technologie mehrsprachige Benutzeroberfläche (USERNAME), die Plattformunterstützung, die sie für die Aktivierung mehrsprachiger Benutzeroberflächen bietet, und die Vorteile, die sie für das Windows Ökosystem bietet.

Gehen Sie auf dieser Seite wie folgt vor:

-   [Der Bedarf an mehrsprachigem Computing](#the-need-for-multilingual-computing)
-   [Die Rolle von MULTILINGUAL bei der Aktivierung von mehrsprachigem Computing](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Grundlegende Konzepte von MUI](#core-concepts-of-mui)
-   [Verlauf der WINDOWS](#history-of-mui-in-windows)
-   [Vorteile der TECHNOLOGY-Technologie](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>Der Bedarf an mehrsprachigem Computing

Um von den Wachstumschancen der internationalen Märkte zu profitieren, unterstützen die Microsoft-Plattformen und -Anwendungen mehr Sprachen, Kulturen und Märkte als je zuvor.

Sprach-, Kultur- und Marktspezifisch sind trotz zunehmender Globalisierungstrends immer noch äußerst relevant für internationale Benutzer. Das folgende Kreisdiagramm zeigt, dass nicht englischsprachige Sprecher immer noch 91,5 Prozent der Bevölkerung der Welt ausmachen.

![Kreisdiagramm mit drei Segmenten; der mit "nicht englische Sprecher 91,5 %" bezeichnete ist deutlich größer als die anderen beiden kombinierten Sprachen.](images/overview-of-mui-fig1.gif)

Weltweit gibt es derzeit 193 Länder und mehr als 6.900 bekannte sprachen, die verwendet werden. Englisch wird trotz seiner Rolle als Geschäftssprache der Welt nur von 8,5 % der Bevölkerung der Welt als erste oder zweite Sprache gesprochen. Um native Informationen für 94 % der Bevölkerung der Welt bereitzustellen, müssen diese Informationen in den 347 (etwa 5 %) der Sprachen der Welt verfügbar sein, die mindestens eine Million Sprecher haben. Dies gilt insbesondere, da Globalisierungstrends die Erwartungen dieser Benutzer in Bezug auf Technologie und ihre Verfügbarkeit in ihren Märkten erhöht haben.

Die Notwendigkeit, Software in mehr Sprachen zu lokalisieren, hat sich im Laufe der Jahre erhöht, und Microsoft stellt jetzt Windows Vista und andere Produkte in mehr Sprachen als je zuvor bereit. Diese Weiterentwicklung ist bei Microsoft Windows besonders deutlich, da sie von der Unterstützung von 30 Sprachen mit Windows 98 zu fast 100 mit Windows Vista übergegangen ist, wie im folgenden Balkendiagramm dargestellt.

![Balkendiagramm, das zeigt, dass die Anzahl der Sprachen in Windows Vista viel größer ist als in Windows 98 oder Windows XP](images/overview-of-mui-fig2.gif)

*Abbildung 2– Anzahl der von Microsoft Windows Releases unterstützten Sprachen*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>Die Rolle von MULTILINGUAL bei der Aktivierung von mehrsprachigem Computing

Wie im vorherigen Abschnitt erläutert, sind [Globalisierung](glossary-for-understanding-mui.md) und [Lokalisierung](glossary-for-understanding-mui.md) von Anwendungen in einer stärker global integrierten Welt zu einer Notwendigkeit geworden. Insbesondere wenn immer mehr Unternehmen global arbeiten , entweder intern oder über ihre Geschäftsnetzwerke, steigt der Bedarf an mehrsprachigen Anwendungen erheblich. Dies sind auch die Hindernisse, mit denen diese Unternehmen derzeit bei der globalen Bereitstellung dieser Anwendungen konfrontiert sind.

Die Bereitstellung von Unterstützung für weitere Sprachen für Windows Betriebssysteme sowie softwarebezogene Anwendungen, die für die Windows Plattform entwickelt wurden, erfordert neue Strategien, mit denen alle wichtigen Szenarien mit minimalem Engineeringaufwand implementiert werden können.

DIE TECHNOLOGY-Technologie richtet sich an Entwickler und ISVs, die mehrsprachige Anwendungen für die Windows-Plattform erstellen und unterstützen möchten. DAS IST auch für OEMs und Unternehmen von entscheidender Bedeutung, die es nutzen können, um das Windows Betriebssystem bereitzustellen und Anwendungen über die Bereitstellung eines einzelnen Images auf Computern in verschiedenen Sprachen hinzuzufügen.

## <a name="core-concepts-of-mui"></a>Grundlegende Konzepte von SICHTEN

Die grundlegende Idee hinter DEM PRINZIP besteht darin, [die Speicherung von lokalisierbaren Ressourcen vom Anwendungsquellcode](mui-fundamental-concepts-explained.md)zu trennen, um jede mehrsprachige Anwendung als Kombination aus einer sprachneutralen Kernbinärdatei und einem Satz sprachspezifischer lokalisierter Ressourcendateien entwerfen zu können.

Nachdem der Anwendungsquellcode getrennt von den lokalisierten Ressourcen gespeichert wurde, ist es einfach, [die entsprechenden lokalisierten Ressourcen](mui-fundamental-concepts-explained.md) für einen bestimmten Anwendungskontext dynamisch zu laden, basierend auf einer Logik, die Einstellungen auf System-, Benutzer- und Anwendungsebene für die Sprache der Benutzeroberfläche berücksichtigt.

Diese grundlegenden Attribute von HELPDESK erleichtern Geschäftsszenarien, z. B.:

-   Ein verbessertes Lokalisierungsmodell für die Benutzeroberfläche und Hilfeinhalte durch die physische Trennung von Anwendungsquellcode und lokalisierbaren Ressourcen.
-   Behandeln der lokalisierbaren Ressourcen als dynamischer Inhalt und Laden dieser Ressourcen gemäß den Einstellungen für die Benutzeroberflächensprache und fallbackeinstellungen. Dies ermöglicht Szenarien wie die folgenden:
    -   Wechseln von einer Benutzeroberflächensprache zu einer anderen zur Laufzeit.
    -   Erstellen von regionalen oder weltweiten Einzelbereitstellungsimages, die eine Reihe von Sprachen für OEMs und Unternehmen abdecken.

## <a name="history-of-mui-in-windows"></a>Verlauf der WINDOWS

Die Unterstützungsebene, die für eine mehrsprachige Benutzeroberfläche auf Windows Betriebssystemebene und für die entwicklung mehrsprachiger Anwendungen auf der Windows Plattform verfügbar ist, hat sich im Laufe der Zeit und in den verschiedenen Versionen von Windows weiterentwickelt.

Die unterstützten Funktionen [vor Windows Vista](evolution-of-mui-support-across-windows-versions.md) waren recht einfach, mit single-language Windows Images und einer Option zum Hinzufügen mehrsprachige Benutzeroberfläche Packs in bestimmten Szenarien. Es war keine Entwicklerunterstützung für mehrsprachige Anwendungen verfügbar.

[Mit Windows Vista](evolution-of-mui-support-across-windows-versions.md)hat Microsoft eine erhebliche Investition in DAS UNTERNEHMEN getätigt, und Windows Vista wird von Grund auf auf einer VISTA-Plattform erstellt. Dies ist zwar ein großer Fortschritt in Windows Lokalisierungsstrategie, da es für Microsoft eine wichtige Möglichkeit ist, Windows in mehr Sprachen als je zuvor bereitzustellen, aber es ist vor allem ein großer Fortschritt für Windows Benutzer, Entwickler und Kunden. Dies bietet mehrere wichtige Vorteile, z. B.:

-   Ein sprachneutrales Betriebssystem mit integrierter Unterstützung für LANGUAGE.
-   Konfigurierbare Paketierung, Bereitstellung und Installation zur Unterstützung mehrsprachiger Szenarien.
-   Einzelimagebereitstellung mit mehreren Sprachen.
-   Ein verbessertes Wartungsmodell, bei dem der ausführbare Code unabhängig von den Ressourcen aktualisiert werden kann.
-   Entwicklerunterstützung für die Erstellung mehrsprachiger Anwendungen.

Die folgende Tabelle enthält eine ausführliche Übersicht über die Windows Plattformunterstützung für TABS:

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Support</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Unterstützte Windows Versionen (nur Betriebssystemunterstützung)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Windows 2000-Serverfamilie</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Windows Server 2003-Produktfamilie</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Unterstützte Windows Versionen (Unterstützung von Betriebssystem-&-Anwendungen)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Nicht Unterstützte Windows-Versionen</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows Ich</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Vorteile der TECHNOLOGY-Technologie

DER POSITIVE Einfluss auf mehrere Aspekte des Windows Ökosystems:

-   [Vorteile für Entwickler:](benefits-of-mui-explained.md)Anwendungsentwickler erhalten zahlreiche Vorteile durch die Verfügbarkeit der UNTERSTÜTZUNG DER API für die ENTWICKLUNG mehrsprachiger Anwendungen, die auf den gleichen Prinzipien wie die mehrsprachige Unterstützung im Kernbetriebssystem Windows Betriebssystem selbst basieren. Zu diesen Vorteilen zählen:
    -   Die Möglichkeit, eine Anzeigesprache bereitzustellen, die mit dem Betriebssystem selbst konsistent ist.
    -   Die Möglichkeit, die Sprachunterstützung für eine Anwendung einfach zu erweitern.
    -   Die Möglichkeit, die Anwendung einfach zu verwalten und zu warten.
    -   Die Möglichkeit, die Einzelimagebereitstellung von Anwendungen durch OEMs zu aktivieren.
-   [Vorteile für Unternehmen:](benefits-of-mui-explained.md)Der hauptvorteil, den DAS UNTERNEHMEN bietet, ist die Möglichkeit, dasselbe mehrsprachige Image weltweit mit einer einzigen Installation herauszuführen, zu unterstützen und zu warten. Ein weiterer wichtiger Gewinn ist die Möglichkeit, mehrsprachige Desktops zu unterstützen, die benutzern mit unterschiedlichen Spracheinstellungen eine nahtlose Interaktion ermöglichen.
-   [Vorteile für OEMs:](benefits-of-mui-explained.md)Der Hauptvorteil für OEMs ist die installation einzelner Images, die VON ERMÖGLICHT wird, mit Unterstützung für mehrere Sprachen, die eine effektivere Verwaltung des Bestands ermöglicht. OEMs profitieren auch von der SUPPORTS-Unterstützung für die Anwendungsentwicklung, da sie es ihnen ermöglichen, Mehrwertanwendungen für ihre Images bereitzustellen und gleichzeitig von der Installation eines einzelnen Images zu profitieren, solange diese Anwendungen MIT AKTIVIERT sind.

 

 




