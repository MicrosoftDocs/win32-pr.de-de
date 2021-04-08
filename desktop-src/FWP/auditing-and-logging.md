---
title: Überwachung
description: Windows-Filter Plattform (WFP) ermöglicht die Überwachung von Firewall-und IPSec-bezogenen Ereignissen.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "103949283"
---
# <a name="auditing"></a>Überwachung

Die Windows-Filter Plattform (WFP) ermöglicht die Überwachung von Firewall-und IPSec-bezogenen Ereignissen. Diese Ereignisse werden im System Sicherheitsprotokoll gespeichert.

Die überwachten Ereignisse lauten wie folgt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie "Überwachung"</th>
<th>Überwachungsunterkategorie</th>
<th>Überwachte Ereignisse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Richtlinienänderung<br/> {6997984d-797a-11d9-bed3-505054503030}<br/></td>
<td>Filtern von Platt Form Richtlinien Änderungen<br/> {0cce9233-69ae-11d9-bed3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Die Zahlen stellen die Ereignis-IDs dar, die von Ereignisanzeige (eventvwr.exe) angezeigt werden.
</blockquote>
<br/> Hinzufügen und Entfernen von WFP-Objekten:<br/>
<ul>
<li>5440 permanente Legende wurde hinzugefügt.</li>
<li>5441 Start-oder persistente Filter hinzugefügt</li>
<li>5442 permanenter Anbieter hinzugefügt</li>
<li>5443 persistenter Anbieter Kontext hinzugefügt</li>
<li>5444 persistente Unterebene hinzugefügt</li>
<li>5446-Lauf Zeit Aufruf hinzugefügt oder entfernt</li>
<li>5447-Lauf Zeitfilter hinzugefügt oder entfernt</li>
<li>5448-Lauf Zeit Anbieter hinzugefügt oder entfernt</li>
<li>5449-Lauf Zeit Anbieter Kontext hinzugefügt oder entfernt</li>
<li>5450-Lauf Zeit Unterschicht hinzugefügt oder entfernt</li>
</ul></td>
</tr>
<tr class="even">
<td>Objektzugriff<br/> {6997984a-797a-11d9-bed3-505054503030}<br/></td>
<td>Filtern von Platt Form Paketen <br/> {0cce9225-69ae-11d9-bed3-505054503030}<br/></td>
<td>Von WFP gelöschte Pakete:<br/>
<ul>
<li>5152 Paket gelöscht</li>
<li>5153 Paket wurde überprüft.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Objektzugriff<br/></td>
<td>Platt Form Verbindung wird gefiltert <br/> {0cce9226-69ae-11d9-bed3-505054503030}<br/></td>
<td>Zulässige und blockierte Verbindungen:<br/>
<ul>
<li>5154 lauschen zulässig</li>
<li>5155 lauschen blockiert</li>
<li>5156 Verbindung zulässig</li>
<li>5157 Verbindung blockiert</li>
<li>5158 Bindung zulässig</li>
<li>5159 Bindung blockiert</li>
</ul>
<blockquote>
[!Note]<br />
Zulässige Verbindungen überwachen nicht immer die ID des zugeordneten Filters. Die Filter-ID für TCP ist 0, es sei denn, es wird eine Teilmenge dieser Filterbedingungen verwendet: UserID, AppID, Protocol, Remoteport.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Objektzugriff<br/></td>
<td>Andere Objekt Zugriffsereignisse<br/> {0cce9227-69ae-11d9-bed3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Diese Unterkategorie ermöglicht viele Überwachungen. Die folgenden WFP-Überwachungen sind unten aufgeführt.
</blockquote>
<br/> Denial-of-Service-Schutzstatus:<br/>
<ul>
<li>5148 WFP-DOS-Präventions Modus wurde gestartet.</li>
<li>5149 der WFP-DOS-Präventions Modus wurde beendet.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anmeldung/Abmeldung<br/> {69979849-797a-11d9-bed3-505054503030}<br/></td>
<td>IPSec-Hauptmodus<br/> {0cce9218-69ae-11d9-bed3-505054503030}<br/></td>
<td>IKE-und AuthIP-Hauptmodusaushandlung:<br/>
<ul>
<li>4650, 4651 Sicherheits Zuordnung eingerichtet</li>
<li>4652, 4653-Aushandlung fehlgeschlagen</li>
<li>4655 Sicherheits Zuordnung beendet</li>
</ul></td>
</tr>
<tr class="even">
<td>Anmeldung/Abmeldung<br/></td>
<td>IPSec-Schnellmodus <br/> {0cce9219-69ae-11d9-bed3-505054503030}<br/></td>
<td>IKE-und AuthIP-Schnellmodus-Aushandlung:<br/>
<ul>
<li>5451 Sicherheits Zuordnung eingerichtet</li>
<li>5452 Sicherheits Zuordnung beendet</li>
<li>4654 Aushandlung fehlgeschlagen</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anmeldung/Abmeldung <br/></td>
<td>Erweiterter IPSec-Modus<br/> {0cce921a-69ae-11d9-bed3-505054503030}<br/></td>
<td>AuthIP-Aushandlung im erweiterten Modus:<br/>
<ul>
<li>4978 ungültiges Aushandlungs Paket.</li>
<li>4979, 4980, 4981, 4982 Sicherheits Zuordnung eingerichtet</li>
<li>4983, 4984-Aushandlung fehlgeschlagen</li>
</ul></td>
</tr>
<tr class="even">
<td>System<br/> {69979848-797a-11d9-bed3-505054503030}<br/></td>
<td>IPSec-Treiber<br/> {0cce9213-69ae-11d9-bed3-505054503030}<br/></td>
<td>Vom IPSec-Treiber gelöschte Pakete:<br/>
<ul>
<li>4963 eingehender Klartext-Paket wurde gelöscht</li>
</ul></td>
</tr>
</tbody>
</table>



 

Standardmäßig ist die Überwachung für WFP deaktiviert.

Die Überwachung kann auf kategoriebasis entweder über das MMC-Snap-in Gruppenrichtlinienobjekt-Editor, über das MMC-Snap-in "lokale Sicherheitsrichtlinie" oder über den auditpol.exe-Befehl aktiviert werden.

Wenn Sie z. b. die Überwachung von Richtlinien Änderungs Ereignissen aktivieren möchten, können Sie Folgendes tun:

-   Verwenden Sie die Gruppenrichtlinienobjekt-Editor

    1.  Führen Sie **gpeer dit. msc** aus.
    2.  Erweitern Sie lokale Computer Richtlinie.
    3.  Erweitern Sie Computer Konfiguration.
    4.  Erweitern Sie Windows-Einstellungen.
    5.  Erweitern Sie Sicherheitseinstellungen.
    6.  Erweitern Sie lokale Richtlinien.
    7.  Klicken Sie auf Überwachungsrichtlinie.
    8.  Doppelklicken Sie auf Überwachungs Richtlinien Änderung, um das Dialogfeld Eigenschaften zu öffnen.
    9.  Aktivieren Sie die Kontrollkästchen erfolgreich und Fehler.

-   Lokale Sicherheitsrichtlinie verwenden

    1.  Führen Sie **secpol. msc** aus.
    2.  Erweitern Sie lokale Richtlinien.
    3.  Klicken Sie auf Überwachungsrichtlinie.
    4.  Doppelklicken Sie auf Überwachungs Richtlinien Änderung, um das Dialogfeld Eigenschaften zu öffnen.
    5.  Aktivieren Sie die Kontrollkästchen erfolgreich und Fehler.

-   Verwenden des Befehls "auditpol.exe"

    -   **Auditpol/Set/Category: "Richtlinien Änderung"/Success: enable/Failure: enable**

Die Überwachung kann nur über den auditpol.exe Befehl auf der Basis einer einzelnen Unterkategorie aktiviert werden.

Die Kategorien "Auditing" und "SubCategory" sind lokalisiert. Um die Lokalisierung für das Überwachen von Skripts zu vermeiden, können die entsprechenden GUIDs anstelle der Namen verwendet werden.

Beispielsweise können Sie einen der folgenden Befehle verwenden, um die Überwachung von Richtlinien Änderungs Ereignissen für Filter Plattformen zu aktivieren:

-   **Auditpol/Set/SubCategory: "Filtern von Platt Form Richtlinien ändern"/Success: enable/Failure: enable**
-   **Auditpol/Set/SubCategory: "{0cce9233-69ae-11d9-bed3-505054503030}"/Success: enable/Failure: enable**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Ereignisprotokoll](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Gruppenrichtlinie](/windows/deployment/deploy-whats-new)
</dt> </dl>

