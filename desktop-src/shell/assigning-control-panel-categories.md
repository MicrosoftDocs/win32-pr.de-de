---
description: Ab Windows XP unterstützt die Systemsteuerung die Kategorisierung von System Steuerungselementen. Elemente werden registriert, damit Sie in einer oder mehreren Kategorien angezeigt werden. Es können keine neuen Kategorien erstellt werden.
title: Zuweisen von System Steuerungs Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977408"
---
# <a name="assigning-control-panel-categories"></a>Zuweisen von System Steuerungs Kategorien

Ab Windows XP unterstützt die Systemsteuerung die Kategorisierung von System Steuerungselementen. Elemente werden registriert, damit Sie in einer oder mehreren Kategorien angezeigt werden. Es können keine neuen Kategorien erstellt werden.

Wenn Sie ein System Steuerungselement in einer oder mehreren Kategorien registrieren möchten, fügen Sie Werte wie im Abschnitt "System [Steuerungs](registering-control-panel-items.md) Element-Registrierung" oder " [dll-System Steuerungselement Registrierung](registering-control-panel-items.md) " unter "Registrieren von [System Steuerungselementen](registering-control-panel-items.md)" beschrieben hinzu.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie-ID</th>
<th>Kategoriename (Windows 7)</th>
<th>Kategoriename (Windows Vista)</th>
<th>Kategoriename (Windows XP)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>&quot;Alle System Steuerungselemente&quot;</td>
<td>&quot;Zusätzliche Optionen&quot;
<blockquote>
[!Note]<br />
In dieser Kategorie wird jedes System Steuerungselement, das keine Kategorie-ID angibt, angezeigt.
</blockquote>
<br/></td>
<td>&quot;Weitere Optionen der Systemsteuerung&quot;
<blockquote>
[!Note]<br />
In dieser Kategorie wird jedes System Steuerungselement, das keine Kategorie-ID angibt, angezeigt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>1</td>
<td>&quot;Darstellung und Personalisierung&quot;</td>
<td>&quot;Darstellung und Personalisierung&quot;</td>
<td>&quot;Darstellung und Designs&quot;</td>
</tr>
<tr class="odd">
<td>2</td>
<td>&quot;Hardware und Sound&quot;</td>
<td>&quot;Hardware und Sound&quot;</td>
<td>&quot;Drucker und andere Hardware&quot;</td>
</tr>
<tr class="even">
<td>3</td>
<td>&quot;Netzwerk und Internet&quot;</td>
<td>&quot;Netzwerk und Internet&quot;</td>
<td>&quot;Netzwerk-und Internet Verbindungen&quot;</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Nicht mehr verwendet. Jedes Element, das sich nur in Kategorie 4 einfügt, wird in Kategorie 2 (Hardware und Sound) angezeigt.</td>
<td>Nicht mehr verwendet. Jedes Element, das sich nur in Kategorie 4 einfügt, wird in Kategorie 2 (Hardware und Sound) angezeigt.</td>
<td>&quot;Sounds, Sprache und Audiogeräte&quot;</td>
</tr>
<tr class="even">
<td>5</td>
<td>&quot;System und Sicherheit&quot;</td>
<td>&quot;System und Wartung&quot;</td>
<td>&quot;Leistung und Wartung&quot;</td>
</tr>
<tr class="odd">
<td>6</td>
<td>&quot;Uhr, Sprache und Region&quot;</td>
<td>&quot;Uhr, Sprache und Region&quot;</td>
<td>&quot;Datum, Uhrzeit, Sprache und regionale Optionen&quot;</td>
</tr>
<tr class="even">
<td>7</td>
<td>&quot;Erleichterte Bedienung&quot;</td>
<td>&quot;Erleichterte Bedienung&quot;</td>
<td>&quot;Barrierefreiheits Optionen&quot;</td>
</tr>
<tr class="odd">
<td>8</td>
<td>&quot;Programs&quot;</td>
<td>&quot;Programs&quot;</td>
<td>&quot;Software&quot;</td>
</tr>
<tr class="even">
<td>9</td>
<td>&quot;User Accounts (Benutzerkonten)&quot;
<blockquote>
[!Note]<br />
Wenn keine Verbindung mit einer Domäne besteht, wird dies als " &quot; Benutzerkonten" und "Familien Sicherheit" bezeichnet &quot; .
</blockquote>
<br/></td>
<td>&quot;User Accounts (Benutzerkonten)&quot;
<blockquote>
[!Note]<br />
Wenn keine Verbindung mit einer Domäne besteht, wird dies als " &quot; Benutzerkonten" und "Familien Sicherheit" bezeichnet &quot; .
</blockquote>
<br/></td>
<td>&quot;User Accounts (Benutzerkonten)&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Nicht mehr verwendet. Die in dieser Kategorie registrierten Elemente werden in Kategorie 5 (System und Sicherheit) angezeigt.</td>
<td>&quot;Security&quot;</td>
<td>&quot;Security Center&quot;
<blockquote>
[!Note]<br />
Nur in Windows XP Service Pack 2 (SP2) oder höher verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>Nicht mehr verwendet. Die in dieser Kategorie registrierten Elemente werden in Kategorie 0 (alle System Steuerungselemente) angezeigt.</td>
<td>&quot;Mobile PCs&quot;
<blockquote>
[!Note]<br />
Diese Kategorie ist nur auf mobilen PCs sichtbar.
</blockquote>
<br/></td>
<td>Nicht verwendet.</td>
</tr>
</tbody>
</table>



 

In Windows XP funktionieren die Kategorien " **Programme** " und " **Benutzerkonten** " unter anderen Kategorien in der Systemsteuerung etwas anders. Wenn einer dieser beiden Kategorien ein oder mehrere Elemente hinzugefügt werden, öffnet der zugehörige Link in der Systemsteuerung eine Kategorieseite. Die registrierten Elemente werden im unteren Teil der Seite unter der Überschrift "oder ein System Steuerungs Symbol auswählen" angezeigt. Wenn keine Elemente für eine dieser Kategorien registriert sind, ruft der zugehörige Link in der Systemsteuerung direkt das standardmäßige Windows-Element für diese Kategorie auf. In Windows Vista und höher verfügen die Kategorie " **Programme** " und die Kategorie " **Benutzerkonten** " nicht über diese Eigenschaft.

Die **Security Center** Kategorie, die nur in Windows XP SP2 verfügbar ist, ist auch etwas nicht standardmäßig. Wenn Sie auf diese Kategorie klicken, wird die Seite **Security Center** in einem neuen Fenster geöffnet. Die für **Security Center** registrierten Elemente werden im unteren Teil der Seite unter der Überschrift **Manage Security Settings for:** angezeigt. Wenn Sie auf ein Symbol klicken, wird das System Steuerungselement geöffnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPlApplet](using-cplapplet.md)
</dt> <dt>

[Nachrichtenverarbeitung in der Systemsteuerung](message-processing.md)
</dt> <dt>

[Ausführen von System Steuerungselementen](executing-control-panel-items.md)
</dt> <dt>

[Erweitern von System Steuerungselementen](extending-system-control-panel-items.md)
</dt> <dt>

[Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




