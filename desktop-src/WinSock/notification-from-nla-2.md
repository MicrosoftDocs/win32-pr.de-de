---
description: NLA ist in der Lage, Clients eine Benachrichtigung über Netzwerkadressen Änderungen bereitzustellen. Der Mechanismus, der zum Anfordern von Benachrichtigungen über Änderungs Ereignisse verwendet wird, ist eine Kombination der Funktionen wsalookupservicebegin, wsanspioctl und WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Benachrichtigung von NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ee0ad0530725db27c8f5df39b6fc573f7e97c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526126"
---
# <a name="notification-from-nla"></a>Benachrichtigung von NLA

NLA ist in der Lage, Clients eine Benachrichtigung über Netzwerkadressen Änderungen bereitzustellen. Der Mechanismus, der zum Anfordern von Benachrichtigungen über Änderungs Ereignisse verwendet wird, ist eine Kombination der Funktionen [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**wsanspioctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)und [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

Um eine Änderungs Benachrichtigung von NLA zu erhalten, muss ein Client zuerst [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) aufrufen, um ein gültiges NLA SP-Nachschlage Handle zu erhalten. Anschließend kann der Client [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) oder [**wsanspioctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) in beliebiger Reihenfolge abrufen. um sich für eine Benachrichtigung zu registrieren, müssen Sie die **wsanspioctl** -Funktion mit dem \_ \_ \_ im Parameter " *dwcontrolcode* " festgelegten Code der "sio NSP Notify Change Control" aufrufen

Die [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktion gibt WSA \_ E \_ nicht \_ mehr als festgelegter Trennzeichen zurück. Wenn ein Client mithilfe der [**wsanspioctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) -Funktion für eine Benachrichtigung registriert wurde und **WSALookupServiceNext** WSA \_ E nicht mehr zurückgibt, gibt der Aufruf von \_ \_ **WSALookupServiceNext** erneut an, ob eine Änderung aufgetreten ist:

-   Wenn seit dem vorherigen WSA e keine Änderungen vorgenommen \_ wurden \_ \_ , wird WSA \_ e \_ nicht \_ mehr zurückgegeben.
-   Wenn eine Änderung aufgetreten ist, oder wenn eine Änderung stattgefunden hat und ein Abruf Vorgang erfolgt ist, gibt der [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) -Funktionsaufrufs Netzwerke als [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Strukturen zurück, wobei eines der folgenden Flags im **dwoutputflags** -Member festgelegt wird:

    <dl> Ergebnis \_ wird \_ hinzugefügt  
    Ergebnis \_ wurde \_ geändert  
    Das Ergebnis \_ ist \_ gelöscht.  
    </dl>

Die Änderungs Benachrichtigung wird für alle Felder bereitgestellt, die sich geändert haben, seit das NLA-Nachschlage Handle mit dem [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktionsbefehl abgerufen wurde, oder seit der letzten Enumeration, die zu dem WSA-Fehler geführt hat, \_ \_ nicht \_ mehr. Wenn alle geänderten Netzwerkadressen Informationen bereitgestellt werden, wird WSA \_ E \_ nicht \_ mehr zurückgegeben. Clients können jederzeit einen [**wsanspioctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) -Funktionsaufruf für das gleiche Abfrage Handle für das gleiche Abfrage handle wiederholen, wobei das \_ sicherheitsflag für die bilitätsnsp- \_ Benachrichtigung \_ festgelegt ist. Diese Funktion ermöglicht es einem Client, das Abfrage handle fortlaufend wiederzuverwenden. Dadurch wird der Client nicht mehr in der Lage sein, Informationen zum Änderungs Zustand selbst zu erhalten. Wenn ein Client keine Änderungs Benachrichtigungen mehr benötigt, sollte er das Abfrage Handle mithilfe der [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Funktion schließen.

 

 



