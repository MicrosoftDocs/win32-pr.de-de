---
description: Wenn die Rückgabeverarbeitungsoption msidbCustomActionTypeContinue nicht festgelegt ist, muss die benutzerdefinierte Aktion einen ganzzahligen Statuscode zurückgeben, wie in der folgenden Tabelle gezeigt.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Rückgabewerte für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3853cfeafba22cb2d479feb1e699c29bcf4b0ab7a08402245f30958cb593df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045000"
---
# <a name="custom-action-return-values"></a>Rückgabewerte für benutzerdefinierte Aktionen

Wenn die **Rückgabeverarbeitungsoption msidbCustomActionTypeContinue** nicht festgelegt ist, muss die benutzerdefinierte Aktion einen ganzzahligen Statuscode zurückgeben, wie in der folgenden Tabelle gezeigt.



| Rückgabewert                 | BESCHREIBUNG                           |
|------------------------------|---------------------------------------|
| FEHLERFUNKTION \_ \_ NICHT \_ AUFGERUFEN | Die Aktion wurde nicht ausgeführt.                  |
| FEHLER \_ ERFOLGREICH               | Aktionen wurden erfolgreich abgeschlossen.       |
| FEHLER \_ BEIM INSTALLIEREN VON \_ USEREXIT     | Der Benutzer hat vorzeitig beendet.          |
| FEHLER \_ BEI DER \_ INSTALLATION      | Nicht behebbarer Fehler.         |
| FEHLER: \_ \_ KEINE ELEMENTE \_ MEHR       | Überspringen Sie die verbleibenden Aktionen, kein Fehler. |



 

Beachten Sie, dass benutzerdefinierte Aktionen, bei denen es [sich um ausführbare Dateien](executable-files.md) handelt, für den Erfolg den Wert 0 zurückgeben müssen. Das Installationsprogramm interpretiert alle anderen Rückgabewerte als Fehler. Um Rückgabewerte zu ignorieren, legen Sie das **Bitflag msidbCustomActionTypeContinue** im Feld Type der [CustomAction-Tabelle fest.](customaction-table.md)

Weitere Informationen zur **Option msidbCustomActionTypeContinue** und zu anderen Rückgabeverarbeitungsoptionen finden Sie unter [Custom Action Return Processing Options](custom-action-return-processing-options.md).

Beachten Sie, Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn der Rückgabewert der Aktion beispielsweise in der Protokolldatei als 1 angezeigt wird, bedeutet dies, dass die Aktion ERROR SUCCESS zurückgegeben \_ hat. Weitere Informationen zu dieser Übersetzung finden Sie unter [Protokollierung von Aktions-Rückgabewerten.](logging-of-action-return-values.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlercodes](error-codes.md)
</dt> <dt>

[Protokollierung von Aktions-Rückgabewerten](logging-of-action-return-values.md)
</dt> </dl>

 

 



