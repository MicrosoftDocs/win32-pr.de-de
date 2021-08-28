---
title: IIS-Protokollierung
description: IiS-Protokollierung ist eine Art von serverseitiger Protokollierung, die für eine URL-Gruppe aktiviert werden kann.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd92582e048a3b1a27d88f50f33c368345c72a836b72de9f2abb777bf5e9c59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102100"
---
# <a name="iis-logging"></a>IIS-Protokollierung

IiS-Protokollierung ist eine Art von serverseitiger Protokollierung, die für eine URL-Gruppe aktiviert werden kann. Das IIS-Protokolldateiformat ist ein festes textbasiertes ASCII-Format, das nicht angepasst werden kann. Die IIS-Protokolldatei enthält die Cachetreffer der HTTP-Server-API im Kernelmodus. Diese Art der Protokollierung kann nur für eine URL-Gruppe aktiviert werden. kann nicht in der Serversitzung verwendet werden.

Das IIS-Protokolldateiformat zeichnet die folgenden Daten auf. Die Daten in der Tabelle liegen in der Reihenfolge des Vorkommens in der Protokolldatei.



| Feld                | BESCHREIBUNG                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client-IP-Adresse    | Die IP-Adresse des Clients, der die Anforderung gestellt hat.                                                                                                                               |
| Benutzername            | Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet. Die bewährte Methode besteht dabei, dass die Anwendung immer den Benutzernamen an die Verfügung stellt. |
| Date                 | Das Datum, an dem die Aktivität aufgetreten ist.                                                                                                                                          |
| Time                 | Die lokale Zeit, zu der die Aktivität aufgetreten ist.                                                                                                                                    |
| Dienst und Instanz | Der Internetdienstname und die Instanznummer, die auf dem Client ausgeführt wurde.                                                                                                     |
| Servername          | Der Name des Servers, auf dem der Protokolldateieintrag generiert wurde.                                                                                                                 |
| IP-Adresse des Servers    | Die IP-Adresse des Servers, auf dem der Protokolldateieintrag generiert wurde.                                                                                                           |
| Benötigte Zeit           | Die Dauer der Aktion in Millisekunden.                                                                                                                         |
| Gesendete Clientbytes    | Die Anzahl der vom Client gesendeten Bytes.                                                                                                                                           |
| Gesendete Serverbytes    | Die Anzahl der vom Server gesendeten Bytes.                                                                                                                                           |
| Dienststatuscode  | Der Wert 200 gibt an, dass die Anforderung erfolgreich erfüllt wurde.                                                                                                             |
| Windows Statuscode  | Der Wert 0 (null) gibt an, dass die Anforderung erfolgreich erfüllt wurde.                                                                                                        |
| Anforderungstyp         | Das Anforderungsverb.                                                                                                                                                                 |
| Ziel des Vorgangs  | Das Ziel des Verbs, z. B. Default.htm.                                                                                                                                 |
| Parameter           | Die Parameter, die an einen Kzip übergeben werden.                                                                                                                                        |



 

Nicht alle Felder enthalten Informationen. Für Felder, für die keine Informationen enthalten sind, wird ein Bindestrich (-) als Platzhalter angezeigt. Wenn ein Feld ein nicht druckbares Zeichen enthält, ersetzt die HTTP-Server-API es durch ein Pluszeichen (+), um das Protokolldateiformat zu erhalten. Dies tritt in der Regel bei Virenangriffen auf, wenn beispielsweise ein böswilliger Benutzer Wagenrücklauf- und Zeilenfeeds sendet, die das Protokolldateiformat nicht durch das Pluszeichen (+) ersetzen würden. Felder werden durch Kommas getrennt, wodurch das Format leichter lesbar ist als die anderen ASCII-Formate, die Leerzeichen für Trennzeichen verwenden. Die Zeit wird als Ortszeit aufgezeichnet. Die zeit in Millisekunden aufgezeichnete Zeit. Weitere Informationen zum Zeitfeld finden Sie im [Thema W3C-Protokollierung.](w3c-logging.md)

Das folgende Beispiel zeigt einen allgemeinen NCSA-Protokolldateieintrag.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




