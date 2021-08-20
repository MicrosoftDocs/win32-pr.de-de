---
title: Überwachung
description: Windows Die Filterplattform (WFP) ermöglicht die Überwachung von Firewall- und IPsec-bezogenen Ereignissen.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 854841685bab015fc0b9a4bc985762df46a7f0c89eae3d38b4b63e081107b70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015408"
---
# <a name="auditing"></a>Überwachung

Die Windows Filterplattform (WFP) ermöglicht die Überwachung von Firewall- und IPsec-bezogenen Ereignissen. Diese Ereignisse werden im Systemsicherheitsprotokoll gespeichert.

Die überwachten Ereignisse sind wie folgt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Überwachungskategorie</th>
<th>Überwachungsunterkategorie</th>
<th>Überwachte Ereignisse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Richtlinienänderung<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtern von Plattformrichtlinienänderungen<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Die Zahlen stellen die Ereignis-IDs dar, die von Ereignisanzeige (eventvwr.exe) angezeigt werden.
</blockquote>
<br/> Hinzufügen und Entfernen von WFP-Objekten:<br/>
<ul>
<li>5440 Persistente Callout hinzugefügt</li>
<li>5441 Startzeit oder persistenter Filter hinzugefügt</li>
<li>5442 Persistenter Anbieter hinzugefügt</li>
<li>5443 Persistenter Anbieterkontext hinzugefügt</li>
<li>5444 Hinzugefügte persistente Unterebene</li>
<li>5446 Laufzeitaufruf hinzugefügt oder entfernt</li>
<li>5447 Laufzeitfilter hinzugefügt oder entfernt</li>
<li>5448 Laufzeitanbieter hinzugefügt oder entfernt</li>
<li>5449 Laufzeitanbieterkontext hinzugefügt oder entfernt</li>
<li>5450 Hinzugefügte oder entfernte untere Laufzeitebene</li>
</ul></td>
</tr>
<tr class="even">
<td>Objektzugriff<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtern des Ablages von Plattformpaketen <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Von WFP gelöschte Pakete:<br/>
<ul>
<li>5152 Verworfenes Paket</li>
<li>5153 Paket übersprengt</li>
</ul></td>
</tr>
<tr class="odd">
<td>Objektzugriff<br/></td>
<td>Filtern der Plattformverbindung <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Zulässige und blockierte Verbindungen:<br/>
<ul>
<li>5154 Lauschen zulässig</li>
<li>5155 Lauschen blockiert</li>
<li>5156 Verbindung zulässig</li>
<li>5157 Verbindung blockiert</li>
<li>5158 Bindung zulässig</li>
<li>5159 Bindung blockiert</li>
</ul>
<blockquote>
[!Note]<br />
Zulässige Verbindungen überwachen nicht immer die ID des zugeordneten Filters. Die FilterID für TCP ist 0, es sei denn, eine Teilmenge dieser Filterbedingungen wird verwendet: UserID, AppID, Protokoll, Remoteport.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Objektzugriff<br/></td>
<td>Andere Objektzugriffsereignisse<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Diese Unterkategorie ermöglicht viele Überwachungen. WFP-spezifische Überwachungen sind unten aufgeführt.
</blockquote>
<br/> Denial-of-Service-Schutzstatus:<br/>
<ul>
<li>5148 WFP DoS-Schutzmodus gestartet</li>
<li>5149 WFP DoS-Schutzmodus beendet</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anmeldung/Abmeldung<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>IPsec-Hauptmodus<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>IKE- und AuthIP-Hauptmodusaushandlung:<br/>
<ul>
<li>4650, 4651 Eingerichtete Sicherheitszuordnung</li>
<li>Fehler bei der Aushandlung 4652, 4653</li>
<li>4655 Sicherheitszuordnung wurde beendet</li>
</ul></td>
</tr>
<tr class="even">
<td>Anmeldung/Abmeldung<br/></td>
<td>IPsec-Schnellmodus <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>IKE- und AuthIP-Schnellmodusaushandlung:<br/>
<ul>
<li>5451 Eingerichtete Sicherheitszuordnung</li>
<li>5452 Sicherheitszuordnung wurde beendet</li>
<li>Fehler bei 4654 Aushandlung</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anmeldung/Abmeldung <br/></td>
<td>Erweiterter IPsec-Modus<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Aushandlung im erweiterten AuthIP-Modus:<br/>
<ul>
<li>4978 Ungültiges Aushandlungspaket</li>
<li>4979, 4980, 4981, 4982 Eingerichtete Sicherheitszuordnung</li>
<li>4983, 4984 Aushandlung fehlgeschlagen</li>
</ul></td>
</tr>
<tr class="even">
<td>System<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>IPsec-Treiber<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Vom IPsec-Treiber gelöschte Pakete:<br/>
<ul>
<li>4963 Eingehendes Klartextpaket gelöscht</li>
</ul></td>
</tr>
</tbody>
</table>



 

Standardmäßig ist die Überwachung für WFP deaktiviert.

Die Überwachung kann pro Kategorie entweder über das Gruppenrichtlinienobjekt-Editor MMC-Snap-In, das MMC-Snap-In für lokale Sicherheitsrichtlinien oder den Befehl auditpol.exe aktiviert werden.

Um beispielsweise die Überwachung von Richtlinienänderungsereignissen zu aktivieren, haben Sie folgende Aktionen:

-   Verwenden der Gruppenrichtlinienobjekt-Editor

    1.  Führen Sie **gpedit.msc aus.**
    2.  Erweitern Sie Richtlinie für lokalen Computer.
    3.  Erweitern Sie Computerkonfiguration.
    4.  Erweitern Sie Windows Einstellungen.
    5.  Erweitern Sie Sicherheit Einstellungen.
    6.  Erweitern Sie Lokale Richtlinien.
    7.  Klicken Sie auf Überwachungsrichtlinie.
    8.  Doppelklicken Sie auf Änderung der Überwachungsrichtlinie, um das Dialogfeld Eigenschaften zu öffnen.
    9.  Aktivieren Sie die Kontrollkästchen Erfolg und Fehler.

-   Verwenden der lokalen Sicherheitsrichtlinie

    1.  Führen Sie **secpol.msc aus.**
    2.  Erweitern Sie Lokale Richtlinien.
    3.  Klicken Sie auf Überwachungsrichtlinie.
    4.  Doppelklicken Sie auf Änderung der Überwachungsrichtlinie, um das Dialogfeld Eigenschaften zu öffnen.
    5.  Aktivieren Sie die Kontrollkästchen Erfolg und Fehler.

-   Verwenden des befehls auditpol.exe

    -   **auditpol /set /category:"Policy Change" /success:enable /failure:enable**

Die Überwachung kann pro Unterkategorie nur über den befehlsbasierten auditpol.exe werden.

Die Namen der Überwachungskategorie und der Unterkategorie werden lokalisiert. Um die Lokalisierung für Überwachungsskripts zu vermeiden, können die entsprechenden GUIDs statt der Namen verwendet werden.

Um beispielsweise die Überwachung von Ereignissen zum Filtern von Plattformrichtlinienänderungsereignissen zu aktivieren, können Sie einen der folgenden Befehle verwenden:

-   **auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**
-   **auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Ereignisprotokoll](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Gruppenrichtlinie](/windows/deployment/deploy-whats-new)
</dt> </dl>

