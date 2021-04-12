---
title: Lauschen auf Menü Band Ereignisse
description: Das Windows-Menü Band Framework verwendet die Infrastruktur der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), damit Entwickler lernen können, wie Benutzer mit dem Menüband Ihrer Anwendung interagieren.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows-Menüband, Ereignisse
- Multifunktionsleiste, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316616"
---
# <a name="listening-for-ribbon-events"></a>Lauschen auf Menü Band Ereignisse

Das Windows-Menü Band Framework verwendet die Infrastruktur der [Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw)](../etw/event-tracing-portal.md) , damit Entwickler lernen können, wie Benutzer mit dem Menüband Ihrer Anwendung interagieren.

## <a name="introduction"></a>Einführung

Der Menüband Framework-Ereignis Mechanismus ist so konzipiert, dass das Framework Multifunktionsleisten-Benutzeroberflächen Ereignisse an die Anwendung meldet, damit Sie die Benutzeraktivität überwachen, ihre Interaktionsmuster erlernen und Verwendungs Trends bewerten können. Diese Informationen können verwendet werden, um die Benutzer Funktionen für zukünftige Iterationen der Menüband-APP zu verfeinern.

Die Verwendung der Menü Band Framework-Ereignisse umfasst Folgendes:

1.  Die Multifunktionsleistenanwendung muss einen [etw-Listener (Event Tracing for Windows, Ereignis Ablauf Verfolgung für Windows)](../etw/event-tracing-portal.md) registrieren, um Benachrichtigungen über das Menüband-Ereignis Benachrichtigungen
2.  Das Menüband Framework löst Ereignis Rückrufe für Multifunktionsleisten-Benutzeroberflächen zur Laufzeit aus, wenn die Anwendung einen [etw-Listener (Event Tracing for Windows)](../etw/event-tracing-portal.md) registriert hat.

## <a name="supported-events"></a>Unterstützte Ereignisse

Die für Menüband-Anwendungen verfügbar gemachten Ereignisse werden in der folgenden Tabelle beschrieben. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ereignis</th>
<th>Ereignisbericht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aktivierte Registerkarte</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignis Verb<br/></td>
</tr>
<tr class="even">
<td>Kontext Registerkarte aktiviert</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignis Verb<br/></td>
</tr>
<tr class="odd">
<td>Anwendungsmenü geöffnet</td>
<td>Ereignis Verb<br/></td>
</tr>
<tr class="even">
<td>Anwendungsmenü geschlossen</td>
<td>Ereignis Verb<br/></td>
</tr>
<tr class="odd">
<td>Menü (regulär oder Galerie) geöffnet</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignis Verb<br/>
<blockquote>
[!Note]<br />
QAT-Menü Ereignisse werden nicht verfügbar gemacht.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menü (regulär oder Katalog) geschlossen</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignis Verb<br/>
<blockquote>
[!Note]<br />
QAT-Menü Ereignisse werden nicht verfügbar gemacht.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Get-Help</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignis Verb<br/> Einer der folgenden Ereignisspeicher Orte:
<ul>
<li>Band</li>
<li>Quickaccesstoolbar</li>
<li>Applicationmenu</li>
<li>Contextpopup</li>
</ul>
<br/> ID des übergeordneten Befehls<br/> Name des übergeordneten Befehls<br/> Eine der folgenden Methoden zum Aufrufen:
<ul>
<li>KLICKEN</li>
<li>KEYTIP</li>
<li>Gewünschte</li>
<li>Ansprechen</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Element Kataloge und Kombinations Felder enthalten den ausgewählten Element Index, enthalten aber keine Zeichen folgen-und ganzzahligen Werte. Spinner enthalten nicht den ganzzahligen Wert.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Multifunktionsleiste minimiert</td>
<td>Ereignis Verb<br/></td>
</tr>
<tr class="odd">
<td>Menü Band erweitert (erweitern Sie die Schaltfläche, auf die geklickt wird oder tippen</td>
<td>Ereignis Verb<br/></td>
</tr>
<tr class="even">
<td>Anwendungsmodus gewechselt</td>
<td>Ereignis Verb<br/> Mode-ID (durch <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>setmodes</strong></a>fest gelegungswert)<br/>
<blockquote>
[!Note]<br />
Die Anwendung ist dafür verantwortlich, diese Ganzzahl zu entpacken, um zu bestimmen, welche Modi festgelegt wurden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickInfo angezeigt</td>
<td>Ereignis Verb<br/> ID des übergeordneten Befehls<br/> Name des übergeordneten Befehls<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickler Handbücher für Windows Ribbon Framework](windowsribbon-guides-entry.md)
</dt> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](./windowsribbon-schema.md)
</dt> <dt>

[Multifunktionsleisten-Benutzeroberflächen Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menüband-Entwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

