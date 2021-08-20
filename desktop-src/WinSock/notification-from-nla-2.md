---
description: Die NLA kann ihren Clients Benachrichtigungen über Änderungen des Netzwerkspeicherorts bereitstellen. Der Mechanismus zum Anfordern von Benachrichtigungen über Änderungsereignisse ist eine Kombination der Funktionen WSALookupServiceBegin, WSANSPIoctl und WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Benachrichtigung von NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8e7309fe6845d822702ffd81448999e2472ebdd37a6949812f622110ee9d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822665"
---
# <a name="notification-from-nla"></a>Benachrichtigung von NLA

Die NLA kann ihren Clients Benachrichtigungen über Änderungen des Netzwerkspeicherorts bereitstellen. Der Mechanismus zum Anfordern von Benachrichtigungen über Änderungsereignisse ist eine Kombination der Funktionen [**WSALookupServiceBegin,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)und [**WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)

Um Änderungsbenachrichtigungen von der NLA zu erhalten, muss ein Client zuerst [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) aufrufen, um ein gültiges NLA-SP-Suchhandle abzurufen. Als Nächstes kann der Client [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) oder [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) in beliebiger Reihenfolge aufrufen. Um sich für Benachrichtigungen zu registrieren, rufen Sie die **WSANSPIoctl-Funktion** mit dem \_ SIO NSP \_ NOTIFY \_ CHANGE-Steuerungscode auf, der im *dwControlCode-Parameter* festgelegt ist.

Die [**WSALookupServiceNext-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) gibt WSA \_ E NO MORE als \_ \_ Set-Trennzeichen zurück. Wenn sich ein Client mithilfe der [**WSANSPIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) für die Benachrichtigung registriert hat und **WSALookupServiceNext** WSA E NO MORE zurückgibt, \_ zeigt der \_ \_ aufrufende **WSALookupServiceNext** erneut an, ob eine Änderung aufgetreten ist:

-   Wenn seit dem vorherigen WSA E NO MORE keine Änderungen vorgenommen \_ \_ \_ wurden, wird WSA \_ E NO MORE \_ \_ zurückgegeben.
-   Wenn eine Änderung aufgetreten ist oder eine Änderung aufgetreten ist und ein Abrufaufruf erfolgt ist, gibt der [**WSALookupServiceNext-Funktionsaufruf**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) Netzwerke als [**WSAQUERYSET-Strukturen**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) zurück, wobei eines der folgenden Flags in seinem **dwOutputFlags-Member** festgelegt ist:

    <dl> ERGEBNIS \_ \_ HINZUGEFÜGT  
    ERGEBNIS \_ \_ GEÄNDERT  
    ERGEBNIS \_ WIRD \_ GELÖSCHT  
    </dl>

Änderungsbenachrichtigungen werden für alle Felder bereitgestellt, die sich seit dem Abrufen des NLA-Suchhandle mit dem [**WSALookupServiceBegin-Funktionsaufruf**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) oder seit der letzten Enumeration geändert haben, die zum \_ WSA E \_ NO \_ MORE-Fehler geführt hat. Wenn alle informationen zum geänderten Netzwerkspeicherort bereitgestellt werden, wird WSA \_ E \_ NO MORE \_ zurückgegeben. Clients können einen [**WSANSPIoctl-Funktionsaufruf**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) für dasselbe Abfragehandle jederzeit nacheinander erneut ausführen, wobei das \_ SIO NSP \_ NOTIFY \_ CHANGE-Flag festgelegt ist. Diese Funktion ermöglicht es einem Client, das Abfragehandle fortlaufend wiederzuverwenden, sodass der Client keine Änderungszustandsinformationen selbst verwalten muss. Sobald ein Client keine Änderungsbenachrichtigungen mehr benötigt, sollte er das Abfragehandle mithilfe der [**WSALookupServiceEnd-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) schließen.

 

 



