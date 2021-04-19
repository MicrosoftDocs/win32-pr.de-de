---
description: Das Installationsprogramm schreibt die folgenden Werte in das Protokoll, wenn eine Aktion diese Fehlercodes zurückgibt. Die gesamte Liste der Fehlercodes, die von den Windows Installer Funktionsaufrufen MsiExec.exe und InstMsi.exe zurückgegeben werden, finden Sie unter Fehlercodes.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Protokollierung von Aktions Rückgabe Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363421"
---
# <a name="logging-of-action-return-values"></a>Protokollierung von Aktions Rückgabe Werten

Das Installationsprogramm schreibt die folgenden Werte in das Protokoll, wenn eine Aktion diese Fehlercodes zurückgibt. Die gesamte Liste der Fehlercodes, die von den Windows Installer Funktionsaufrufen MsiExec.exe und InstMsi.exe zurückgegeben werden, finden Sie unter [Fehlercodes](error-codes.md).



| Fehlercode                       | Von Funktionsaufrufen zurückgegebene Werte MsiExec.exe und InstMsi.exe | Werte, die im Protokoll angezeigt werden. | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler \_ Funktion \_ nicht \_ aufgerufen     | 1626                                                           | 0                              | Eine Funktion konnte nicht ausgeführt werden.                                                                                                                                                                                                                                               |
| Fehler \_ erfolgreich                   | 0                                                              | 1                              | Eine Aktion wurde erfolgreich abgeschlossen.                                                                                                                                                                                                                                               |
| Fehler beim \_ Installieren von \_ Userexit.         | 1602                                                           | 2                              | Ein Benutzer hat die Installation abgebrochen.                                                                                                                                                                                                                                                   |
| Fehler bei der \_ Installation. \_          | 1603                                                           | 3                              | Ein schwerwiegender Fehler.                                                                                                                                                                                                                                                                  |
| Fehler beim \_ Installieren von \_ Suspend          | 1604                                                           | 4                              | Die Installation wurde angehalten, unvollständig.                                                                                                                                                                                                                                         |
| Fehler \_ erfolgreich                   | 0                                                              | 5                              | Die Aktion wurde erfolgreich abgeschlossen.                                                                                                                                                                                                                                              |
| Fehler bei \_ ungültigem \_ handle- \_ Status    | 1609                                                           | 6                              | Das Handle befindet sich in einem ungültigen Zustand.                                                                                                                                                                                                                                              |
| \_ungültige \_ Daten             | 1626                                                           | 7                              | Die Daten sind ungültig.                                                                                                                                                                                                                                                            |
| Fehler \_ Installation wird \_ bereits \_ ausgeführt. | 1618                                                           | 8                              | Eine weitere Installation erfolgt gerade. In den Tabellen [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) können jeweils nur eine Installation Aktionen ausführen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer Protokollierung](windows-installer-logging.md)
</dt> </dl>

 

 



