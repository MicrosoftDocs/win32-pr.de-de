---
title: Lauschen auf Menübandereignisse
description: Das Windows-Menübandframework verwendet die ETW-Infrastruktur (Event Tracing for Windows), damit Entwickler erfahren können, wie Benutzer mit dem Menüband ihrer Anwendung interagieren.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Menüband,Ereignisse
- Menüband,Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9519553a40cd613085949d4650c2689e817f387e47e9ab4380b629464e90d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202970"
---
# <a name="listening-for-ribbon-events"></a>Lauschen auf Menübandereignisse

Das Windows-Menübandframework verwendet die [ETW-Infrastruktur (Event Tracing for Windows),](../etw/event-tracing-portal.md) damit Entwickler erfahren können, wie Benutzer mit dem Menüband ihrer Anwendung interagieren.

## <a name="introduction"></a>Einführung

Der Ereignismechanismus für das Menübandframework ist so konzipiert, dass das Framework Ereignisse der Menübandbenutzeroberfläche an die Anwendung meldet, sodass Sie Benutzeraktivitäten überwachen, ihre Interaktionsmuster erlernen und Nutzungstrends bewerten können. Diese Informationen können verwendet werden, um die Benutzerfreundlichkeit für zukünftige Iterationen Ihrer Menüband-App zu optimieren.

Die Verwendung der Frameworkereignisse des Menübands umfasst Folgendes:

1.  Die Menübandanwendung muss einen [ETW-Listener (Event Tracing for Windows)](../etw/event-tracing-portal.md) registrieren, um Menübandereignisbenachrichtigungen vom Menübandframework zu empfangen.
2.  Das Menübandframework gibt Ereignisrückrufe der Menübandbenutzeroberfläche zur Laufzeit aus, wenn die Anwendung einen [ETW-Listener (Event Tracing for Windows) registriert](../etw/event-tracing-portal.md) hat.

## <a name="supported-events"></a>Unterstützte Ereignisse

Die Ereignisse, die für Menübandanwendungen verfügbar gemacht werden, werden in der folgenden Tabelle beschrieben. 

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
<td>Tabulator aktiviert</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignisverb<br/></td>
</tr>
<tr class="even">
<td>Kontextbezogene Registerkarte aktiviert</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignisverb<br/></td>
</tr>
<tr class="odd">
<td>Anwendungsmenü geöffnet</td>
<td>Ereignisverb<br/></td>
</tr>
<tr class="even">
<td>Anwendungsmenü geschlossen</td>
<td>Ereignisverb<br/></td>
</tr>
<tr class="odd">
<td>Menü (normal oder Katalog) geöffnet</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignisverb<br/>
<blockquote>
[!Note]<br />
QAT-Menüereignisse werden nicht verfügbar gemacht.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menü (normal oder Katalog) geschlossen</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignisverb<br/>
<blockquote>
[!Note]<br />
QAT-Menüereignisse werden nicht verfügbar gemacht.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Befehl</td>
<td>Befehls-ID<br/> Befehlsname<br/> Ereignisverb<br/> Einer der folgenden Ereignisstandorte:
<ul>
<li>Bändchen</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> Id des übergeordneten Befehls<br/> Name des übergeordneten Befehls<br/> Eine der folgenden Aufrufmethoden:
<ul>
<li>KLICKEN</li>
<li>Keytip</li>
<li>Tastatur</li>
<li>Touch</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Elementgalerien und Kombinationsfelder enthalten den ausgewählten Elementindex, jedoch keine Zeichenfolgen- und Ganzzahlwerte. Spinner enthalten nicht den ganzzahligen Wert.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menüband minimiert</td>
<td>Ereignisverb<br/></td>
</tr>
<tr class="odd">
<td>Erweitertes Menüband (Schaltfläche erweitern angeklickt oder angeheftet)</td>
<td>Ereignisverb<br/></td>
</tr>
<tr class="even">
<td>Anwendungsmodus umgeschaltet</td>
<td>Ereignisverb<br/> Modus-ID (Durch <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes festgelegter Wert)</strong></a><br/>
<blockquote>
[!Note]<br />
Die Anwendung ist dafür verantwortlich, diese ganze Zahl zu entpacken, um zu bestimmen, welche Modi festgelegt wurden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickInfo angezeigt</td>
<td>Ereignisverb<br/> Id des übergeordneten Befehls<br/> Name des übergeordneten Befehls<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Entwicklerhandbücher für Menübandframework](windowsribbon-guides-entry.md)
</dt> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](./windowsribbon-schema.md)
</dt> <dt>

[Richtlinien für die Benutzerfreundlichkeit des Menübands](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menübandentwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

