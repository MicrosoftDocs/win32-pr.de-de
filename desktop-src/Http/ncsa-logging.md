---
title: NCSA-Protokollierung
description: Die erweiterte NCSA-Protokollierung ist eine Art der serverseitigen Protokollierung, die für eine URL-Gruppe aktiviert werden kann.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5b9ef608da18264f4534c7e50e9672794a21bc61c91741feeb9e814c7afc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078310"
---
# <a name="ncsa-logging"></a>NCSA-Protokollierung

Die erweiterte NCSA-Protokollierung ist eine Art der serverseitigen Protokollierung, die für eine URL-Gruppe aktiviert werden kann. Das NCSA Common-Protokolldateiformat ist ein festes textbasiertes ASCII-Format, das nicht angepasst werden kann. Die NCSA-Protokolldatei enthält die Cachetreffer im Kernelmodus der HTTP-Server-API. Dieser Protokollierungstyp kann nur für eine URL-Gruppe aktiviert werden. sie kann nicht in der Serversitzung verwendet werden.

Das NCSA Common-Protokolldateiformat zeichnet die folgenden Daten auf. Die Daten in der Tabelle werden in der Reihenfolge des Vorkommens in der Protokolldatei angezeigt.



| Feld                                            | BESCHREIBUNG                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Remotehostadresse                              | Die IP-Adresse des Clients, der die Anforderung gestellt hat.                                                                                                                               |
| Remoteprotokollname                                  | Wird nicht verwendet. Dieser Wert ist immer ein Bindestrich.                                                                                                                                          |
| Benutzername                                        | Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet. Die bewährte Methode besteht darin, dass die Anwendung immer den Benutzernamen bereitstellt. |
| Gmt-Offset (Datum, Uhrzeit und Greenwich Mean Time) | Das lokale Datum und die lokale Uhrzeit, zu der die Aktivität aufgetreten ist. Der Offset von Greenwich Mean Time wird ebenfalls angegeben.                                                                    |
| Anforderungs- und Protokollversion                     | Die vom Client verwendete HTTP-Protokollversion.                                                                                                                                   |
| Dienststatuscode                              | Der HTTP-Statuscode. (Der Wert 200 gibt an, dass die Anforderung erfolgreich abgeschlossen wurde.)                                                                                         |
| Gesendete Bytes                                       | Die Anzahl der vom Server gesendeten Bytes.                                                                                                                                           |



 

Nicht alle Felder enthalten Informationen. Für Felder, für die keine Informationen vorhanden sind, wird ein Bindestrich (-) als Platzhalter angezeigt. Wenn ein Feld ein nicht druckbares Zeichen enthält, ersetzt die HTTP-Server-API es durch ein Pluszeichen (+), um das Protokolldateiformat beizubehalten. Dies tritt in der Regel bei Virenangriffen auf, wenn z. B. ein böswilliger Benutzer Wagenrückläufe und Zeilenvorleitungen sendet, die das Protokolldateiformat unterbrechen würden, wenn sie nicht durch das Pluszeichen (+) ersetzt würden. Felder werden durch Leerzeichen getrennt, und die Zeit wird als Ortszeit mit dem GMT-Offset aufgezeichnet.

Das folgende Beispiel zeigt einen NCSA Common-Protokolldateieintrag, der in einem Text-Editor angezeigt wird.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

Die IP-Adresse des Clients lautet 172.21.13.45, und der Benutzername lautet Microsoft \\ JohnDoe. Das Protokoll wurde am 7. April 2005 um 17:39:04 Uhr Ortszeit mit einem Greenwich-Offset von 8 Stunden aufgezeichnet. Das Anforderungsverb und die Protokollversion waren "GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0". Die Statuscodes waren 200 OK, und die Anzahl der vom Client gesendeten Bytes betrug 3401.

 

 




