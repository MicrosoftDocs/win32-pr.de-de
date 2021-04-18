---
title: IIS-Protokollierung
description: IIS-Protokollierung ist eine Art serverseitiger Protokollierung, die für eine URL-Gruppe aktiviert werden kann.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d438d0926be2579fa526cc126c7f635a6eecd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338610"
---
# <a name="iis-logging"></a>IIS-Protokollierung

IIS-Protokollierung ist eine Art serverseitiger Protokollierung, die für eine URL-Gruppe aktiviert werden kann. Das IIS-Protokolldatei Format ist ein festes, textbasiertes ASCII-Format, das nicht angepasst werden kann. Die IIS-Protokolldatei enthält die HTTP-Server-API-Kernel Modus-Cache Treffer. Diese Art der Protokollierung kann nur für eine URL-Gruppe aktiviert werden. Sie kann nicht in der Server Sitzung verwendet werden.

Das IIS-Protokolldatei Format zeichnet die folgenden Daten auf. Die Daten in der Tabelle befinden sich in der angegebenen Reihenfolge in der Protokolldatei.



| Feld                | BESCHREIBUNG                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client-IP-Adresse    | Die IP-Adresse des Clients, der die Anforderung gestellt hat.                                                                                                                               |
| Benutzername            | Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet. Die bewährte Vorgehensweise besteht darin, dass die Anwendung immer den Benutzernamen bereitstellt. |
| Date                 | Das Datum, an dem die Aktivität aufgetreten ist.                                                                                                                                          |
| Time                 | Die Ortszeit, zu der die Aktivität aufgetreten ist.                                                                                                                                    |
| Dienst und Instanz | Der Internet Dienst Name und die Instanznummer, die auf dem Client ausgeführt wurden.                                                                                                     |
| Servername          | Der Name des Servers, auf dem der Protokolldatei Eintrag generiert wurde.                                                                                                                 |
| IP-Adresse des Servers    | Die IP-Adresse des Servers, auf dem der Protokolldatei Eintrag generiert wurde.                                                                                                           |
| Benötigte Zeit           | Die Dauer der Aktion in Millisekunden.                                                                                                                         |
| Gesendete Client Bytes    | Die Anzahl der vom Client gesendeten Bytes.                                                                                                                                           |
| Gesendete Server Bytes    | Die Anzahl der vom Server gesendeten Bytes.                                                                                                                                           |
| Dienststatus Code  | Der Wert 200 gibt an, dass die Anforderung erfolgreich ausgeführt wurde.                                                                                                             |
| Windows-Statuscode  | Der Wert 0 (null) gibt an, dass die Anforderung erfolgreich ausgeführt wurde.                                                                                                        |
| Anforderungstyp         | Das Anforderungs Verb.                                                                                                                                                                 |
| Ziel des Vorgangs  | Das Ziel des Verbs, z. b. Default.htm.                                                                                                                                 |
| Parameter           | Die Parameter, die an eine Scrip-Tabelle übermittelt werden.                                                                                                                                        |



 

Nicht alle Felder enthalten Informationen. Für Felder, für die keine Informationen vorhanden sind, wird ein Bindestrich (-) als Platzhalter angezeigt. Wenn ein Feld ein nicht druckbares Zeichen enthält, wird es von der HTTP-Server-API durch ein Pluszeichen (+) ersetzt, um das Protokolldatei Format beizubehalten. Dies tritt in der Regel bei Virenangriffen auf, wenn z. b. ein böswilliger Benutzer Wagen Rückläufe und Zeilen Feeds sendet, die, wenn Sie nicht durch das Pluszeichen (+) ersetzt werden, das Protokolldatei Format sprengen würden. Felder werden durch Kommas getrennt, sodass das Format leichter lesbar ist als bei den anderen ASCII-Formaten, die Leerzeichen als Trennzeichen verwenden. Die Zeit wird als lokale Zeit aufgezeichnet. Die benötigte Zeit wird in Millisekunden aufgezeichnet. Weitere Informationen zum ergriffene Zeit Feld finden Sie im Thema zur [W3C-Protokollierung](w3c-logging.md) .

Das folgende Beispiel zeigt einen allgemeinen NCSA-Protokolldatei Eintrag.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




