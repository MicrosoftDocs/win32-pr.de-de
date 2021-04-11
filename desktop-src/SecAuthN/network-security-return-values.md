---
description: Rückgabewerte, die von einem Netzwerkanbieter festgelegt werden können.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Rückgabewerte für die Netzwerksicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a362fde712d2a44565894aceb9d85172e488b53a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960335"
---
# <a name="network-security-return-values"></a>Rückgabewerte für die Netzwerksicherheit

Die Rückgabewerte, die von einem Netzwerkanbieter festgelegt werden können, sind die folgenden Fehlercodes.



| Fehlercodes         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN \_ erfolgreich         | Die Funktion wurde erfolgreich ausgeführt.                                                                                                                                                                                                                                                                                                                 |
| WN \_ nicht \_ unterstützt  | Die Funktion wird von diesem Netzwerkanbieter nicht unterstützt.                                                                                                                                                                                                                                                                                 |
| WN- \_ net- \_ Fehler      | Unbekannter Netzwerkfehler.                                                                                                                                                                                                                                                                                                       |
| \_Weitere \_ Daten      | Der Datenpuffer, der in der Übergabe enthalten ist, reicht nicht aus, um alle verfügbaren Daten aufzunehmen.                                                                                                                                                                                                                                                         |
| Ungültiger Zeiger für WN \_ \_    | Während des Funktions Aufrufes wurde ein ungültiger Zeiger angegeben.                                                                                                                                                                                                                                                                     |
| Ungültiger WN- \_ \_ Wert      | Während des Funktions Aufrufes wurde ein ungültiger numerischer Wert angegeben.                                                                                                                                                                                                                                                               |
| Ungültiges \_ \_ Kennwort   | Es wurde ein falsches Kennwort angegeben.                                                                                                                                                                                                                                                                                                    |
| WN- \_ Zugriff \_ verweigert  | Der Aufrufer verfügt nicht über ausreichende Berechtigungen, um den Vorgang abzuschließen.                                                                                                                                                                                                                                                              |
| WN- \_ Funktion \_ ausgelastet  | Diese Funktion kann nicht erneut eingegeben werden und wird zurzeit verwendet, oder der Anbieter wird noch initialisiert und ist noch nicht zum Aufrufen bereit. Der Anbieter sollte diesen Fehlercode nur zurückgeben, wenn er verfügbar sein wird. Dieser Rückgabecode wird von der MPR an seinen Aufrufer zurückgegeben und bewirkt wahrscheinlich, dass der Aufrufer erneut versucht.<br/> |
| Fehler bei WN- \_ Windows \_  | Eine erforderliche Funktion ist fehlgeschlagen.                                                                                                                                                                                                                                                                                                             |
| Ungültiger \_ \_ Benutzer       | Es wurde ein ungültiger Benutzername angegeben.                                                                                                                                                                                                                                                                                            |
| WN \_ nicht genügend Arbeits \_ \_ Speicher | Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.                                                                                                                                                                                                                                                                                 |
| WN \_ nicht \_ verbunden  | Das Gerät wird nicht umgeleitet.                                                                                                                                                                                                                                                                                                           |
| \_geöffnete \_ Dateien in WN     | Die Verbindung konnte nicht abgebrochen werden, da Dateien noch geöffnet sind.                                                                                                                                                                                                                                                                      |
| WN ungültiger \_ \_ NetName    | Der Netzwerkname ist ungültig.                                                                                                                                                                                                                                                                                                          |



 

 

 




