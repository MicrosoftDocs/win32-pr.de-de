---
description: ICE44 überprüft, ob im Dialogfeld "newdialog", "spawndialog" und "spawnwaitdialog" auf gültige Dialogfelder in der Dialogfeld Tabelle verwiesen wird.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362566"
---
# <a name="ice44"></a>ICE44

ICE44 überprüft, ob im Dialogfeld " [newdialog](newdialog-controlevent.md)", " [spawndialog](spawndialog-controlevent.md)" und " [spawnwaitdialog](spawnwaitdialog-controlevent.md) " auf gültige Dialogfelder in der [Dialogfeld Tabelle](dialog-table.md)verwiesen wird.

## <a name="result"></a>Ergebnis

ICE44 gibt eine Fehlermeldung aus, wenn ein Dialogfeld-Steuerelement vorhanden ist, das nicht auf ein Dialogfeld verweist, das in der Dialogfeld Tabelle aufgeführt ist.

## <a name="example"></a>Beispiel

ICE44 würde die folgenden Fehler für das gezeigte Beispiel melden.



| ICE44-Fehler                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Steuerungs Ereignis für das Steuerelement "Dialog1". Control1 ' ist vom Typ spawndialog, das Argument Dialog2 ist jedoch kein gültiger Eintrag in der Dialog Feld Tabelle. | Es gibt eine spawndialog-, spawnwaitdialog-oder newdialog-Aktion, die ein Argument aufweist, das in der Dialogfeld Tabelle nicht auf ein Dialogfeld verweist. Fügen Sie ein Argument hinzu, das ein Schlüssel in der Dialog Feld Tabelle ist, um diesen Fehler zu beheben.<br/> |



 

[Dialog Feld Tabelle](dialog-table.md) (teilweise)



| Dialog  | Titel |
|---------|-------|
| Dialog1 |       |



 

[ControlEvent-Tabelle](controlevent-table.md) (partiell)



| Dialog\_ | Steuerelement\_ | type        | Argument |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | Spawndialog | Dialog2  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




