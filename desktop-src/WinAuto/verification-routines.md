---
title: Überprüfungs Routinen
description: In diesem Abschnitt werden die Überprüfungs Routinen beschrieben, die die UI-Zugriffs Prüfung ausführen kann, um die Barrierefreiheits Implementierung einer Anwendung zu testen.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310148"
---
# <a name="verification-routines"></a>Überprüfungs Routinen

In diesem Abschnitt werden die Überprüfungs Routinen beschrieben, die die UI-Zugriffs Prüfung ausführen kann, um die Barrierefreiheits Implementierung einer Anwendung zu testen.



<table>
<thead>
<tr class="header">
<th>Category</th>
<th>-Routine zurückgegebener Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Konsistenz</strong>$ {Remove} $<br />
</td>
<td><strong>Screenreader</strong></td>
<td>Kompiliert alle sichtbaren Elemente im Überprüfungs Ziel und zeigt Sie in einem ListView-Steuerelement in der Reihenfolge an, in der Sie einem Benutzer von einem Standard Bildschirm Reader angekündigt werden.</td>
</tr>
<tr class="even">
<td><strong>Uiaskrerereader</strong></td>
<td>Identisch mit <strong>Screenreader</strong>, aber für UIA-Implementierungen.</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>Navigation</strong>$ {Remove} $<br />
</td>
<td><strong>Checktreetiefe</strong></td>
<td>Sendet Tabstopps (oder Umschalt + Tab-Zeichen) als Eingabe an das Überprüfungs Ziel, um zu bestätigen, dass die Benutzeroberfläche des Ziels nicht übermäßig Komplex ist oder nicht auf die standardmäßige Tastaturnavigation zugreifen kann.</td>
</tr>
<tr class="even">
<td><strong>Checktabbinguia</strong></td>
<td>Sendet Tabstopps (oder Umschalt + Tab-Zeichen) als Eingabe an das Überprüfungs Ziel, um zu bestätigen, dass alle fokussierbaren Elemente in der Benutzeroberfläche mithilfe der Standardtastatur Navigation ordnungsgemäß und logisch erreichbar sind.</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Eigenschaften</strong>$ {Remove} $<br />
</td>
<td><strong>Checkrole</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche eine gültige, logische MSAA-Rolle meldet und dass das Steuerelement über einen Wert verfügt, der für diese Rolle erforderlich ist.</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen MSAA-Zustand meldet.</td>

</tr>
<tr class="odd">
<td><strong>CheckName</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen MSAA-Namen meldet.</td>

</tr>
<tr class="even">
<td><strong>Checkaccesskeys</strong></td>
<td>Bestätigt, dass Zugriffsschlüssel, die Elementen im Überprüfungs Ziel zugewiesen sind, innerhalb des Überprüfungs Ziels eindeutig sind.</td>

</tr>
<tr class="odd">
<td><strong>Checkboundingrect</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche über ein Begrenzungs Rechteck verfügt, das als Ziel für Treffer Tests verwendet werden kann.</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Tree</strong>$ {Remove} $<br />
</td>
<td><strong>Checkparser</strong></td>
<td>Übergeordnete und untergeordnete Beziehungen in der-Elementstruktur sind konsistent und vorhersagbar.</td>
</tr>
<tr class="odd">
<td><strong>Checkwaisen Children</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche ein gültiges MSAA-übergeordnetes Element meldet.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>UIA-Eigenschaften</strong>$ {Remove} $<br />
</td>
<td><strong>Checknameuia</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen UIA-Namen meldet.</td>
</tr>
<tr class="odd">
<td><strong>Checktreedepthuia</strong></td>
<td>Sendet Tabstopps (oder Umschalt + Tab-Zeichen) als Eingabe an das Überprüfungs Ziel, um zu bestätigen, dass die UIA-Elemente in der Benutzeroberfläche des Ziels nicht übermäßig komplex sind oder nicht auf die standardmäßige Tastaturnavigation zugreifen können.</td>

</tr>
<tr class="even">
<td><strong>CheckStatus</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen UIA-Zustand meldet.</td>

</tr>
<tr class="odd">
<td><strong>Checkaccesskeysuia</strong></td>
<td>Bestätigt, dass neben geordnete Elemente nicht denselben Zugriffs-und/oder Zugriffstasten aufweisen.</td>

</tr>
<tr class="even">
<td><strong>Checkboundingrectuia</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare UIA-Element in der Benutzeroberfläche über ein Begrenzungs Rechteck verfügt, das als Ziel für Treffer Tests verwendet werden kann.</td>

</tr>
<tr class="odd">
<td><strong>Checkcontroltypeuia</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen UIA-Steuer Elementtyp meldet.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>UIA</strong>-Struktur $ {Remove} $<br />
</td>
<td><strong>Checknavigateuia</strong></td>
<td>Bestätigt, dass der UIA TreeWalker durch die untergeordneten Elemente eines Elements navigieren kann.</td>
</tr>
<tr class="odd">
<td><strong>Checkwaisen-Kinder</strong></td>
<td>Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche ein gültiges UIA-übergeordnetes Element meldet.</td>

</tr>
<tr class="even">
<td><strong>Checksiblingsuia</strong></td>
<td>Bestätigt, dass neben geordnete Elemente nicht denselben Namen haben: ControlType-Paare und keine der gleichen automationids.</td>

</tr>
<tr class="odd">
<td>$ {ROWSPAN9} $<strong>Aria Web verifications</strong>$ {Remove} $<br />
</td>
<td><strong>Checkariarole</strong></td>
<td>Bestätigt, dass alle Elemente über eine gültige Aria-Rolle verfügen. Das zugehörige HTML-Tag und die Aria-Rolle sind Informationselemente, bei denen ungültige Rollen als Fehler gekennzeichnet sind.</td>
</tr>
<tr class="even">
<td><strong>Checklabel</strong></td>
<td>Bestätigt, dass jedes Element mit Eingabe, Schaltfläche, Bild Schaltfläche oder der Rolle "Landmark" über eine Bezeichnung verfügt.</td>

</tr>
<tr class="odd">
<td><strong>Checkrangecontrols</strong></td>
<td>Bestätigt Bereichs Steuerelemente mit dem Schieberegler oder der Statusanzeige Rolle sind die richtigen Aria-Attribute definiert.</td>

</tr>
<tr class="even">
<td><strong>Checkcontainerrole</strong></td>
<td>Bestätigt, dass ein Element, oder mindestens eines seiner untergeordneten Elemente, OnKeyDown/OnKeyPress definiert hat.</td>

</tr>
<tr class="odd">
<td><strong>Checklayoutfähig</strong></td>
<td>Bestätigt, dass ein Tabellenlayout eine Zusammenfassung/Th/Aria-DescribedBy enthält.</td>

</tr>
<tr class="even">
<td><strong>Checkgridstructure</strong></td>
<td>Bestätigt, dass ein nicht Tabellen Element mit der Raster Rolle über eine Struktur von Raster>Zeile>gridcell mit zugeordneten Attributen verfügt.</td>

</tr>
<tr class="odd">
<td><strong>Checkdatdatababel</strong></td>
<td>Bestätigt die Eigenschaften von Datentabellen.</td>

</tr>
<tr class="even">
<td><strong>Checkactivedescendants</strong></td>
<td>Bestätigt die Eigenschaften von Elementen mit einem aktiven Nachfolger, der definiert ist.</td>

</tr>
<tr class="odd">
<td><strong>Checkelementswithclickhandler</strong></td>
<td>Bestätigt den Registerkarten Index von Elementen mit Klick Handlern.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Webüberprüfungen</strong>$ {Remove} $<br />
</td>
<td><strong>Checkhtml (Web)</strong></td>
<td>Bestätigt verschiedene HTML-Merkmale, wie z. b. Header, Name, Rahmen und Titel.</td>
</tr>
<tr class="odd">
<td><strong>Checkname (Web)</strong></td>
<td>Bestätigt namens Merkmale, wie z. b. Länge, ungültige Zeichen und Rollen Einbindung.</td>

</tr>
<tr class="even">
<td><strong>Checkrole (Web)</strong></td>
<td>Bestätigt ungültige Rollen, Rollen, die Werte aufweisen sollten und/oder Rollen nicht implementiert sind.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




