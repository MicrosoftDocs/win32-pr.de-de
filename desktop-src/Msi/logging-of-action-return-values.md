---
description: Der Installer schreibt die folgenden Werte in das Protokoll, wenn eine Aktion diese Fehlercodes zurückgibt. Die gesamte Liste der Fehlercodes, die von der Funktion Windows Installer zurückgegeben werden, ruft MsiExec.exe und InstMsi.exe Fehlercodes auf.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Protokollierung von Aktions-Rückgabewerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 756fa633ef486c3dae4b689acf439f8dbf7786c20f740fb4784de30e764dc9fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945895"
---
# <a name="logging-of-action-return-values"></a>Protokollierung von Aktions-Rückgabewerten

Der Installer schreibt die folgenden Werte in das Protokoll, wenn eine Aktion diese Fehlercodes zurückgibt. Die gesamte Liste der Fehlercodes, die von der Funktion Windows Installer zurückgegeben werden, ruft MsiExec.exe und InstMsi.exe [fehlercodes auf.](error-codes.md)



| Fehlercode                       | Von Funktionsaufrufen zurückgegebene MsiExec.exe und InstMsi.exe | Werte, die im Protokoll angezeigt werden. | Beschreibung                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLERFUNKTION \_ \_ NICHT \_ AUFGERUFEN     | 1626                                                           | 0                              | Eine Funktion konnte nicht ausgeführt werden.                                                                                                                                                                                                                                               |
| FEHLER \_ ERFOLGREICH                   | 0                                                              | 1                              | Eine Aktion wurde erfolgreich abgeschlossen.                                                                                                                                                                                                                                               |
| FEHLER \_ BEIM INSTALLIEREN VON \_ USEREXIT         | 1602                                                           | 2                              | Ein Benutzer hat die Installation abgebrochen.                                                                                                                                                                                                                                                   |
| FEHLER \_ BEI DER \_ INSTALLATION          | 1603                                                           | 3                              | Schwerwiegender Fehler.                                                                                                                                                                                                                                                                  |
| FEHLER \_ BEIM INSTALLIEREN VON \_ "SUSPEND"          | 1604                                                           | 4                              | Die Installation wurde angehalten, unvollständig.                                                                                                                                                                                                                                         |
| FEHLER \_ ERFOLGREICH                   | 0                                                              | 5                              | Die Aktion wurde erfolgreich abgeschlossen.                                                                                                                                                                                                                                              |
| FEHLER: \_ \_ UNGÜLTIGER \_ HANDLEZUSTAND    | 1609                                                           | 6                              | Das Handle befindet sich in einem ungültigen Zustand.                                                                                                                                                                                                                                              |
| FEHLER \_ UNGÜLTIGE \_ DATEN             | 1626                                                           | 7                              | Die Daten sind ungültig.                                                                                                                                                                                                                                                            |
| FEHLER: \_ INSTALLATION \_ WIRD BEREITS \_ AUSGEFÜHRT | 1618                                                           | 8                              | Eine weitere Installation erfolgt gerade. Nur eine Installation gleichzeitig kann Aktionen in den Tabellen [InstallExecuteSequence,](installexecutesequence-table.md) [AdminExecuteSequence](adminexecutesequence-table.md)oder [AdvtExecuteSequence](advtexecutesequence-table.md) ausführen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Protokollierung des Installationsprogramms](windows-installer-logging.md)
</dt> </dl>

 

 



