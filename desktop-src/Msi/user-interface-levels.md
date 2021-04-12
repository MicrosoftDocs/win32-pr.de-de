---
description: Windows Installer bietet Paket Entwicklern die Möglichkeit, eine interne Benutzeroberfläche zu erstellen, die über mehrere Funktionsebenen verfügt.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Benutzeroberflächen Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218516"
---
# <a name="user-interface-levels"></a>Benutzeroberflächen Ebenen

Windows Installer bietet Paket Entwicklern die Möglichkeit, eine interne Benutzeroberfläche zu erstellen, die über mehrere Funktionsebenen verfügt. Da die interne Benutzeroberfläche vom Autor des Pakets erstellt werden muss, hängt das Verhalten der vollständigen Benutzeroberfläche, der reduzierten Benutzeroberfläche, der Standardbenutzer Oberfläche und der Ebene "None" vom Installationspaket ab. In der folgenden Tabelle werden die Funktionen beschrieben, die häufig für UI-Ebenen bezeichnet werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>UI-Ebene</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vollständige Benutzeroberfläche</td>
<td>Zeigt modale und nicht modale Dialogfelder an, die in der internen Benutzeroberfläche erstellt wurden. Zeigt die <a href="error-dialog.md">Dialog</a> Felder der erstellten Fehler an.
<blockquote>
[!Note]<br />
Modale Dialogfelder erfordern Benutzereingaben, bevor die Installation fortgesetzt werden kann. Sie werden durch Festlegen des <a href="modal-dialog-style-bit.md">modalen Dialog Felds Bit</a> in der Spalte Attribute der <a href="dialog-table.md">Dialog</a> Tabelle angegeben. Für ein nicht modalem Dialogfeld sind keine Benutzereingaben erforderlich, damit die Installation fortgesetzt werden kann.
</blockquote>
<br/> Eine vollständige Benutzeroberfläche zeigt im Allgemeinen das <a href="user-interface-wizard-behavior.md">Verhalten der Benutzeroberfläche</a>an.<br/></td>
</tr>
<tr class="even">
<td>Reduzierte Benutzeroberfläche</td>
<td>Zeigt alle nicht modalem Dialogfelder an, die in der Benutzeroberfläche erstellt wurden. In werden keine erstellten modalen Dialogfelder angezeigt. Zeigt die <a href="error-dialog.md">Dialog</a> Felder der erstellten Fehler an. Zeigt <a href="authoring-disk-prompt-messages.md">Eingabe</a> Aufforderungs Meldungen an. Zeigt <a href="filesinuse-dialog.md">FilesInUse-Dialog</a> Felder an.</td>
</tr>
<tr class="odd">
<td>Standardbenutzeroberfläche</td>
<td>Zeigt die integrierten Dialogfelder ohne Modus an, in denen Statusmeldungen angezeigt werden. Zeigt integrierte Fehler Dialogfelder an. In werden keine erstellten Dialogfelder angezeigt. Fordert Benutzer auf, einen Datenträger einzufügen, indem ein Dialogfeld mit dem Wert der <a href="diskprompt.md"><strong>diskprompt</strong></a> -Eigenschaft angezeigt wird.</td>
</tr>
<tr class="even">
<td>Keine</td>
<td>None bedeutet eine unbeaufsichtigte Installation, die keine Benutzeroberfläche anzeigt.</td>
</tr>
</tbody>
</table>



 

Die Ebene der internen Benutzeroberfläche kann mithilfe von " [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)" festgelegt werden. Der Installer legt die [**uilevel**](uilevel.md) -Eigenschaft auf die aktuelle Ebene der Benutzeroberfläche fest.

Wenn die [**limitui**](limitui.md) -Eigenschaft festgelegt ist, ist die Benutzeroberflächen Ebene, die bei der Installation des Pakets verwendet wird, auf Basic beschränkt.

Ein Beispiel für die Benutzeroberflächen Erstellung finden Sie unter [einem Installations Beispiel](an-installation-example.md).

 

 




