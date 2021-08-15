---
description: Gibt Werte zurück, die ein Netzwerkanbieter festlegen kann.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Rückgabewerte für die Netzwerksicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40fd8e6e21d9e7671c1e7b9c3d008978628e28cb0fcb01c3df56359144e72e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921299"
---
# <a name="network-security-return-values"></a>Rückgabewerte für die Netzwerksicherheit

Die Rückgabewerte, die ein Netzwerkanbieter festlegen kann, enthalten die folgenden Fehlercodes.



| Fehlercodes         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN \_ SUCCESS         | Die Funktion wurde erfolgreich ausgeführt.                                                                                                                                                                                                                                                                                                                 |
| WN \_ WIRD NICHT \_ UNTERSTÜTZT  | Die Funktion wird für diesen Netzwerkanbieter nicht unterstützt.                                                                                                                                                                                                                                                                                 |
| WN \_ \_ NET-FEHLER      | Ein unbekannter Netzwerkfehler ist aufgetreten.                                                                                                                                                                                                                                                                                                       |
| WN \_ WEITERE \_ DATEN      | Der übergebene Datenpuffer reicht nicht aus, um alle verfügbaren Daten zu enthalten.                                                                                                                                                                                                                                                         |
| WN \_ BAD \_ POINTER    | Ein ungültiger Zeiger wurde während des Funktionsaufrufs angegeben.                                                                                                                                                                                                                                                                     |
| \_UNGÜLTIGER \_ WN-WERT      | Während des Funktionsaufrufs wurde ein ungültiger numerischer Wert angegeben.                                                                                                                                                                                                                                                               |
| UNGÜLTIGES \_ \_ WN-KENNWORT   | Ein falsches Kennwort wurde angegeben.                                                                                                                                                                                                                                                                                                    |
| \_WN-ZUGRIFF \_ VERWEIGERT  | Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Abschließen des Vorgangs.                                                                                                                                                                                                                                                              |
| \_WN-FUNKTION \_ AUSGELASTET  | Diese Funktion kann nicht erneut aufgerufen werden und wird derzeit verwendet, oder der Anbieter wird noch initialisiert und kann noch nicht aufgerufen werden. Der Anbieter sollte diesen Fehlercode nur zurückgeben, wenn er verfügbar sein soll. Dieser Rückgabecode wird vom MPR zurück an den Aufrufer übergeben und führt wahrscheinlich dazu, dass der Aufrufer den Vorgang erneut versucht.<br/> |
| \_ \_ WN-WINDOWS-FEHLER  | Fehler bei einer erforderlichen Funktion.                                                                                                                                                                                                                                                                                                             |
| WN \_ BAD \_ USER       | Ein ungültiger Benutzername wurde angegeben.                                                                                                                                                                                                                                                                                            |
| WN \_ \_ NICHT GENÜGEND \_ ARBEITSSPEICHER | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang abzuschließen.                                                                                                                                                                                                                                                                                 |
| WN \_ NICHT \_ VERBUNDEN  | Das Gerät wird nicht umgeleitet.                                                                                                                                                                                                                                                                                                           |
| WN \_ OPEN \_ FILES     | Die Verbindung konnte nicht abgebrochen werden, da die Dateien noch geöffnet sind.                                                                                                                                                                                                                                                                      |
| WN \_ BAD \_ NETNAME    | Der Netzwerkname ist ungültig.                                                                                                                                                                                                                                                                                                          |



 

 

 




