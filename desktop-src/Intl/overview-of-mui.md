---
description: Dieses Thema enthält eine konzeptionelle Übersicht über die Technologie für mehrsprachige Benutzeroberflächen (MUI), die Platt Form Unterstützung, die für die Aktivierung mehrsprachiger Benutzererfahrung bietet, und die Vorteile, die es für das Windows-Ökosystem bietet.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Übersicht über MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565512"
---
# <a name="overview-of-mui"></a>Übersicht über MUI

Dieses Thema enthält eine konzeptionelle Übersicht über die Technologie für mehrsprachige Benutzeroberflächen (MUI), die Platt Form Unterstützung, die für die Aktivierung mehrsprachiger Benutzererfahrung bietet, und die Vorteile, die es für das Windows-Ökosystem bietet.

Gehen Sie auf dieser Seite wie folgt vor:

-   [Die Notwendigkeit für mehrsprachige Computing](#the-need-for-multilingual-computing)
-   [Die Rolle von MUI beim Aktivieren von mehrsprachigem Computing](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Grundlegende Konzepte von MUI](#core-concepts-of-mui)
-   [Verlauf von MUI in Windows](#history-of-mui-in-windows)
-   [Vorteile der MUI-Technologie](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>Die Notwendigkeit für mehrsprachige Computing

Um von den in internationalen Märkten dargestellten Wachstumschancen zu profitieren, unterstützen die Plattformen und Anwendungen von Microsoft mehr Sprachen, Kulturen und Märkten als je zuvor.

Die Besonderheiten von Sprache, Kultur und Markt sind trotz zunehmender Globalisierungstrends weiterhin für internationale Benutzer äußerst wichtig. Das folgende Kreis Diagramm zeigt, dass nicht englische Referenten nach wie vor 91,5 Prozent der Bevölkerung der Welt ausmachen.

![Kreis Diagramm mit drei Segmenten; die Bezeichnung "nicht englischsprachige Sprecher 91,5%" ist weitaus größer als die beiden anderen, kombiniert](images/overview-of-mui-fig1.gif)

Weltweit sind heute 193 Länder und mehr als 6.900 bekannte lebende Sprachen verfügbar. Englisch, trotz seiner Rolle als Geschäftssprache der Welt, wird nur von 8,5% der Bevölkerung der Welt als erste oder zweite Sprache gesprochen. Um systemeigene Informationen für 94% der Einwohner Welt bereitzustellen, müssen diese Informationen in 347 (ca. 5%) verfügbar sein. der Sprachen der Welt, die über mindestens eine Million Referenten verfügen. Dies trifft vor allem dann zu, wenn Globalisierungstrends die Erwartungen dieser Benutzer hinsichtlich der Technologie und ihrer Verfügbarkeit in ihren Märkten gesteigert haben.

Die Notwendigkeit, Software in mehr Sprachen zu lokalisieren, hat sich im Laufe der Jahre gesteigert, und Microsoft stellt nun Windows Vista und andere Produkte in mehr Sprachen bereit als je zuvor. Diese Entwicklung ist insbesondere bei Microsoft Windows eindeutig, da es von der Unterstützung von 30 Sprachen mit Windows 98 bis fast 100 mit Windows Vista ging, wie im folgenden Balkendiagramm veranschaulicht.

![Balkendiagramm, das anzeigt, dass die Anzahl der Sprachen in Windows Vista viel größer ist als in Windows 98 oder Windows XP](images/overview-of-mui-fig2.gif)

*Abbildung 2 – Anzahl der von Microsoft Windows-Versionen unterstützten Sprachen*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>Die Rolle von MUI beim Aktivieren von mehrsprachigem Computing

Wie bereits im vorherigen Abschnitt erläutert wurde, sind [Globalisierung](glossary-for-understanding-mui.md) und [Lokalisierung](glossary-for-understanding-mui.md) von Anwendungen in einer global integrierten Welt zu einer Notwendigkeit geworden. Da immer mehr Unternehmen sowohl intern als auch über Ihre Unternehmensnetzwerke Global sind, wird der Bedarf an mehrsprachigen Anwendungen erheblich erhöht. Dies sind die Hürden, die diese Unternehmen bei der globalen Bereitstellung dieser Anwendungen unterliegen.

Um Unterstützung für mehr Sprachen für Windows-Betriebssysteme sowie für die Windows-Plattform entwickelte Softwareanwendungen bereitzustellen, sind neue Strategien erforderlich, mit denen alle wichtigen Szenarien mit minimalem Engineering-Aufwand implementiert werden können.

Die MUI-Technologie richtet sich an Entwickler und ISVs, die auf die Erstellung und Unterstützung mehrsprachiger Anwendungen für die Windows-Plattform abzielen. MUI ist auch eine wichtige Bedeutung für OEMs und Unternehmen, die Sie zum Bereitstellen des Windows-Betriebssystems und zum Hinzufügen von Anwendungen zu Computern in verschiedenen Sprachen durch Bereitstellung mit nur einem Image nutzen können.

## <a name="core-concepts-of-mui"></a>Grundlegende Konzepte von MUI

Die grundlegende Idee hinter MUI besteht darin, [den Speicher Lokalisier barer Ressourcen aus dem](mui-fundamental-concepts-explained.md)Quellcode der Anwendung zu trennen, damit jede mehrsprachige Anwendung als eine Kombination aus einer sprach neutralen kernbinär Datei und einer Reihe von sprachspezifischen lokalisierten Ressourcen Dateien konzipiert werden kann.

Sobald der Quellcode der Anwendung getrennt von den lokalisierten Ressourcen gespeichert wird, ist es einfach, [die geeigneten lokalisierten Ressourcen](mui-fundamental-concepts-explained.md) für einen bestimmten Anwendungskontext dynamisch zu laden, basierend auf einer Logik, die System-, Benutzer-und Anwendungsebene für die Benutzeroberflächen Sprache berücksichtigt.

Diese grundlegenden Attribute von MUI helfen, Geschäftsszenarien wie z. b.:

-   Ein verbessertes Lokalisierungs Modell für die Benutzeroberfläche und den Hilfe Inhalt über die physische Trennung von Quellcode der Anwendung und Lokalisier barer Ressourcen.
-   Behandeln Lokalisier barer Ressourcen als dynamischer Inhalt und Laden dieser Ressourcen entsprechend den Einstellungen der Benutzeroberflächen Sprache und den Fall Back Einstellungen. Dies ermöglicht Szenarien wie z. b.:
    -   Wechseln zur Laufzeit von einer Benutzeroberflächen Sprache zu einer anderen.
    -   Erstellen regionaler oder weltweit einstellungsimages, die eine Reihe von Sprachen für OEMs und Unternehmen abdecken.

## <a name="history-of-mui-in-windows"></a>Verlauf von MUI in Windows

Die Unterstützung für mehrsprachige Benutzer auf der Windows-Betriebssystemebene und für die mehrsprachige Anwendungsentwicklung auf der Windows-Plattform hat sich im Laufe der Zeit und über die verschiedenen Versionen von Windows entwickelt.

Die unterstützte Funktionalität [vor Windows Vista](evolution-of-mui-support-across-windows-versions.md) war relativ einfach, mit einsprachigen Windows-Images und einer Option zum Hinzufügen von mehrsprachigen Benutzerschnittstellen Paketen in bestimmten Szenarien. Es war keine Entwickler Unterstützung für mehrsprachige Anwendungen verfügbar.

[Mit Windows Vista](evolution-of-mui-support-across-windows-versions.md)machte Microsoft bedeutende Investitionen in MUI, und Windows Vista wurde von Grund auf auf einer MUI-Plattform erstellt. Obwohl dies ein wichtiger Fortschritt bei der Windows-Lokalisierungsstrategie darstellt, ist es ein wichtiger Faktor für Microsoft, Windows in mehr Sprachen als je zuvor bereitzustellen, und es ist vor allem eine gute Voraussetzung für Windows-Benutzer,-Entwickler und-Kunden. Dies bietet verschiedene wichtige Vorteile, wie z. b.:

-   Ein sprach neutrales Betriebssystem mit integrierter Unterstützung für MUI.
-   Konfigurierbare Paket Erstellung, Bereitstellung und Installation, um mehrsprachige Szenarien zu unterstützen.
-   Bereitstellung mit einem Bild mit mehreren Sprachen.
-   Ein verbessertes Wartungs Modell, bei dem der ausführbare Code unabhängig von den Ressourcen aktualisiert werden kann.
-   Entwickler Unterstützung zum entwickeln mehrsprachiger Anwendungen.

In der folgenden Tabelle finden Sie eine ausführliche Übersicht über die Unterstützung der Windows-Plattform für MUI:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Support</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Unterstützte Windows-Versionen (nur Betriebssystemunterstützung)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Windows 2000-Server Familie</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Windows Server 2003-Produktfamilie</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Unterstützte Windows-Versionen (Unterstützung für Betriebssystem & Anwendungen)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Nicht Unterstützte Windows-Versionen</td>
<td><ul>
<li>Windows 9X</li>
<li>Windows Me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Vorteile der MUI-Technologie

MUI wirkt sich positiv auf mehrere Aspekte des Windows-Ökosystems aus:

-   [Vorteile für Entwickler](benefits-of-mui-explained.md): zahlreiche Vorteile von Anwendungsentwicklern durch die Verfügbarkeit der MUI-API-Unterstützung, um mehrsprachige Anwendungen zu erstellen, die auf denselben Prinzipien basieren wie die mehrsprachige Unterstützung im Windows-Kernbetriebssystem. Zu diesen Vorteilen zählen:
    -   Die Möglichkeit, eine Anzeige Sprache bereitzustellen, die mit den Funktionen des Betriebssystems konsistent ist.
    -   Die Möglichkeit, die Sprachunterstützung für eine Anwendung auf einfache Weise zu erweitern.
    -   Die Möglichkeit, die Anwendung leicht zu verwalten und zu warten.
    -   Die Möglichkeit, die Bereitstellung von Anwendungen mit nur einem Image durch OEMs zu aktivieren.
-   [Vorteile für Unternehmen](benefits-of-mui-explained.md): der größte Vorteil, den MUI für Unternehmen bietet, ist die Möglichkeit, das gleiche mehrsprachige Image weltweit mit einer einzelnen Installation einzuführen, zu unterstützen und zu pflegen. Ein weiterer bedeutender Gewinn ist die Möglichkeit, mehrsprachige Desktops zu unterstützen, die eine nahtlose Interaktion mit Benutzern mit unterschiedlichen Spracheinstellungen ermöglichen.
-   [Vorteile für OEMs](benefits-of-mui-explained.md): der größte Vorteil für OEMs ist die Installation mit einem einzelnen Image, die MUI ermöglicht, mit Unterstützung für mehrere Sprachen, die eine effektivere Verwaltung der Inventur ermöglicht. OEMs profitieren auch von der MUI-Unterstützung für die Anwendungsentwicklung, da Sie Ihnen die Bereitstellung von Mehrwert Anwendungen auf Ihren Images ermöglicht, während Sie von der Installation mit einem einzelnen Image profitieren, solange diese Anwendungen MUI-fähig sind.

 

 




