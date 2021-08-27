---
description: Windows Das Installationsprogramm bietet Paketentwicklern die Möglichkeit, eine interne Benutzeroberfläche zu erstellen, die über mehrere Funktionalitätsebenen verfügt.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Benutzeroberfläche Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbe932ea10b62d20ca06a027b935ff04289cdef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478066"
---
# <a name="user-interface-levels"></a>Benutzeroberfläche Ebenen

Windows Das Installationsprogramm bietet Paketentwicklern die Möglichkeit, eine interne Benutzeroberfläche zu erstellen, die über mehrere Funktionalitätsebenen verfügt. Da die interne Benutzeroberfläche vom Autor des Pakets erstellt werden muss, hängt das Verhalten der Ebenen vollständige Benutzeroberfläche, reduzierte Benutzeroberfläche, Einfache Benutzeroberfläche und Keine vom Installationspaket ab. In der folgenden Tabelle werden die Funktionen beschrieben, die benutzeroberflächenebenen häufig zugeschrieben werden.




| Benutzeroberflächenebene | BESCHREIBUNG | 
|----------|-------------|
| Vollständige Benutzeroberfläche | Zeigt modale und moduslose Dialogfelder an, die in der internen Benutzeroberfläche verfasst wurden. Zeigt die Dialogfelder <a href="error-dialog.md">für den erstellungsbeladenen</a> Fehler an.<blockquote>[!Note]<br />Modale Dialogfelder erfordern Benutzereingaben, bevor die Installation fortgesetzt werden kann, und werden durch Festlegen des <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in der Spalte Attribute der Tabelle <a href="dialog-table.md">Dialog</a> angegeben. Ein nicht modusloses Dialogfeld erfordert keine Benutzereingaben, damit die Installation fortgesetzt werden kann.</blockquote><br /> Eine vollständige Benutzeroberfläche weist in der Regel Benutzeroberfläche <a href="user-interface-wizard-behavior.md">Assistentenverhalten auf.</a><br /> | 
| Reduzierte Benutzeroberfläche | Zeigt alle nicht moduslosen Dialogfelder an, die in der Benutzeroberfläche verfasst wurden. Es werden keine selbst verfassten modalen Dialogfelder angezeigt. Zeigt die Dialogfelder <a href="error-dialog.md">für den erstellungsbeladenen</a> Fehler an. Zeigt <a href="authoring-disk-prompt-messages.md">Datenträger-Eingabeaufforderungsmeldungen</a> an. Zeigt <a href="filesinuse-dialog.md">FilesInUse-Dialogfelder</a> an. | 
| Standardbenutzeroberfläche | Zeigt die integrierten dialogfelder ohne Modus an, in denen Statusmeldungen angezeigt werden. Zeigt integrierte Fehlerdialogfelder an. Es werden keine selbst verfassten Dialogfelder angezeigt. Fordert Benutzer zum Einfügen eines Datenträgers auf, indem ein Dialogfeld mit dem <a href="diskprompt.md"><strong>DiskPrompt-Eigenschaftswert</strong></a> angezeigt wird. | 
| Keine | Keine bedeutet eine automatische Installation, bei der keine Benutzeroberfläche angezeigt wird. | 




 

Die Ebene der internen Benutzeroberfläche kann mit [**msiSetInternalUI festgelegt werden.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) Das Installationsprogramm legt die [**UILevel-Eigenschaft**](uilevel.md) auf die aktuelle Ebene der Benutzeroberfläche fest.

Wenn die [**LIMITUI-Eigenschaft**](limitui.md) festgelegt ist, ist die Benutzeroberflächenebene, die beim Installieren des Pakets verwendet wird, auf Basic beschränkt.

Ein Beispiel für die Benutzeroberflächenerstellung finden Sie unter [Beispiel für eine Installation.](an-installation-example.md)

 

 




