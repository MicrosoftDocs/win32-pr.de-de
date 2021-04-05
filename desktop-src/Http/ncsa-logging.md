---
title: NCSA-Protokollierung
description: Die erweiterte NCSA-Protokollierung ist eine Art der serverseitigen Protokollierung, die für eine URL-Gruppe aktiviert werden kann.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04db62d5d561fb227f7a46a33c2aefcacd943b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713955"
---
# <a name="ncsa-logging"></a>NCSA-Protokollierung

Die erweiterte NCSA-Protokollierung ist eine Art der serverseitigen Protokollierung, die für eine URL-Gruppe aktiviert werden kann. Das allgemeine NCSA-Protokolldatei Format ist ein festes, textbasiertes ASCII-Format, das nicht angepasst werden kann. Die NCSA-Protokolldatei enthält die HTTP-Server-API-Kernel Modus-Cache Treffer. Diese Art der Protokollierung kann nur für eine URL-Gruppe aktiviert werden. Sie kann nicht in der Server Sitzung verwendet werden.

Das allgemeine NCSA-Protokolldatei Format zeichnet die folgenden Daten auf. Die Daten in der Tabelle befinden sich in der angegebenen Reihenfolge in der Protokolldatei.



| Feld                                            | BESCHREIBUNG                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Remote Host Adresse                              | Die IP-Adresse des Clients, der die Anforderung gestellt hat.                                                                                                                               |
| Remote Protokoll Name                                  | Nicht verwendet. Dieser Wert ist immer ein Bindestrich.                                                                                                                                          |
| Benutzername                                        | Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet. Die bewährte Vorgehensweise besteht darin, dass die Anwendung immer den Benutzernamen bereitstellt. |
| Datum, Uhrzeit und Greenwich Mean Time (GMT) Offset | Der lokale Zeitpunkt (Datum und Uhrzeit), zu dem die Aktivität aufgetreten ist. Der Offset von der Greenwich Mean-Zeit wird ebenfalls angegeben.                                                                    |
| Anforderungs-und Protokollversion                     | Die vom Client verwendete HTTP-Protokollversion.                                                                                                                                   |
| Dienststatus Code                              | Der HTTP-Statuscode. (Der Wert 200 gibt an, dass die Anforderung erfolgreich abgeschlossen wurde.)                                                                                         |
| Gesendete Bytes                                       | Die Anzahl der vom Server gesendeten Bytes.                                                                                                                                           |



 

Nicht alle Felder enthalten Informationen. Für Felder, für die keine Informationen vorhanden sind, wird ein Bindestrich (-) als Platzhalter angezeigt. Wenn ein Feld ein nicht druckbares Zeichen enthält, wird es von der HTTP-Server-API durch ein Pluszeichen (+) ersetzt, um das Protokolldatei Format beizubehalten. Dies tritt in der Regel bei Virenangriffen auf, wenn z. b. ein böswilliger Benutzer Wagen Rückläufe und Zeilen Feeds sendet, die, wenn Sie nicht durch das Pluszeichen (+) ersetzt werden, das Protokolldatei Format sprengen würden. Felder werden durch Leerzeichen getrennt, und die Uhrzeit wird als lokale Zeit mit dem GMT-Offset aufgezeichnet.

Das folgende Beispiel zeigt einen allgemeinen NCSA-Protokolldatei Eintrag, der in einem Text-Editor angezeigt wird.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

Die IP-Adresse des Clients lautet 172.21.13.45, und der Benutzername lautet Microsoft \\ JohnDoe. Das Protokoll wurde am 7. April 2005 um 17:39:04 Uhr Ortszeit mit einem Greenwich Offset von 8 Stunden aufgezeichnet. Das Anforderungs Verb und die Protokollversion waren "Get/Scripts/IISAdmin/ism.dll? http/Serv HTTP/1.0". Die Statuscodes waren 200 OK, und die Anzahl der vom Client gesendeten Bytes betrug 3401.

 

 




