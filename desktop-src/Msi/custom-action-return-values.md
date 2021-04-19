---
description: Wenn die msidbcustomaction typecontinue-Rückgabe Verarbeitungsoption nicht festgelegt ist, muss die benutzerdefinierte Aktion einen ganzzahligen Statuscode zurückgeben, wie in der folgenden Tabelle gezeigt.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Rückgabewerte für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363781"
---
# <a name="custom-action-return-values"></a>Rückgabewerte für benutzerdefinierte Aktionen

Wenn die **msidbcustomaction typecontinue** -Rückgabe Verarbeitungsoption nicht festgelegt ist, muss die benutzerdefinierte Aktion einen ganzzahligen Statuscode zurückgeben, wie in der folgenden Tabelle gezeigt.



| Rückgabewert                 | BESCHREIBUNG                           |
|------------------------------|---------------------------------------|
| Fehler \_ Funktion \_ nicht \_ aufgerufen | Die Aktion wurde nicht ausgeführt.                  |
| Fehler \_ erfolgreich               | Aktionen erfolgreich abgeschlossen.       |
| Fehler beim \_ Installieren von \_ Userexit.     | Der Benutzer wurde vorzeitig beendet.          |
| Fehler bei der \_ Installation. \_      | Nicht BEHEB barer Fehler.         |
| Fehler \_ keine \_ weiteren \_ Elemente       | Überspringen Sie die restlichen Aktionen und keinen Fehler. |



 

Beachten Sie, dass benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, für Erfolg den Wert 0 zurückgeben müssen. Der Installer interpretiert jeden anderen Rückgabewert als Fehler. Wenn Sie Rückgabewerte ignorieren möchten, legen Sie das **msidbcustomaction typecontinue** -Bitflag im type-Feld der [CustomAction-Tabelle](customaction-table.md)fest.

Weitere Informationen zur Option " **msidbcustomaction typecontinue** " und anderen Optionen zur Rückgabe Verarbeitung finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

Beachten Sie, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn der Rückgabewert der Aktion z. b. als 1 in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion Fehler erfolgreich zurückgegeben hat \_ . Weitere Informationen zu dieser Übersetzung finden Sie [unter Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlercodes](error-codes.md)
</dt> <dt>

[Protokollierung von Aktions Rückgabe Werten](logging-of-action-return-values.md)
</dt> </dl>

 

 



