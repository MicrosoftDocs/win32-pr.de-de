---
description: Beim Zugriff auf einen WMI-Server (Windows Management Instrumentation) mit einem Skript können Sie zwischen NT LAN Manager (NTLM) oder Kerberos-Authentifizierungsprotokollen wählen.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Festlegen des Authentifizierungsdiensts mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 837a69df251b5bbb6cc8bef5ac0b882349fde74646ac6ed33149978b8f69ad7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315387"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Festlegen des Authentifizierungsdiensts mit VBScript

Beim Zugriff auf einen WMI-Server (Windows Management Instrumentation) mit einem Skript können Sie zwischen NT LAN Manager (NTLM) oder Kerberos-Authentifizierungsprotokollen wählen. Die Angabe von Kerberos ist nur bei Verwendung der Delegierung erforderlich. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit einer dritten Computerdelegierung.](connecting-to-a-3rd-computer-delegation.md)

Da sich die Betriebssystemversionen darin unterscheiden, welcheN Authentifizierungsdienst sie verwenden, wird empfohlen, beim Herstellen einer Verbindung mit einem Remotesystem keinen Wert für das Autoritätsfeld anzugeben. Lassen Sie stattdessen zu, dass das Betriebssystem und die verteilte Version von Component Object Model (DCOM) NTLM oder Kerberos auswählen. Wenn ein Authentifizierungsdienst angegeben wird, erfordert die Syntax den Serverprinzipalnamen, d. h. den Namen des Zielcomputers anstelle des Domänencontrollers.

Sie können den Authority-Parameter nur mit Verbindungen mit WMI-Remoteservern verwenden. Der Verbindungsversuch schlägt fehl, wenn Sie versuchen, Autorisierungsebenen als Teil eines Monikers oder mit einem Aufruf von [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) für eine lokale Verbindung festzulegen.

Führen Sie das folgende Verfahren aus, um den Authentifizierungsdienst anzugeben, den Sie im *strAuthority-Parameter* der [**SWbemLocator.ConnectServer-Methode**](swbemlocator-connectserver.md) oder der [Monikerzeichenfolgenverbindung](constructing-a-moniker-string.md) verwenden möchten.

**So geben Sie die NTLM- oder Kerberos-Authentifizierung mit der Skripterstellungs-API für WMI an**

1.  Wenn der *strAuthority-Parameter* mit der Zeichenfolge "kerberos:" beginnt, geht WMI davon aus, dass die Zeichenfolge auf einen Kerberos-Prinzipalnamen verweist und die Kerberos-Authentifizierung verwendet wird. Wenn der *strAuthority-Parameter* mit der Zeichenfolge "ntlmdomain:" beginnt, verwendet WMI stattdessen die NTLM-Authentifizierung.
2.  Alternativ können Sie den Autoritätsteil eines Monikers verwenden, um den Authentifizierungstyp anzugeben, der zum Herstellen einer Verbindung mit WMI verwendet wird. Um die Kerberos-Authentifizierung bei Verwendung eines Monikers zu verwenden, schließen Sie die Zeichenfolge "authority=kerberos:" gefolgt vom Prinzipalnamen ein. Um die NTLM-Authentifizierung zu verwenden, schließen Sie die Zeichenfolge "authority=ntlmdomain:" gefolgt vom NTLM-Domänennamen ein.

    Das folgende Beispiel zeigt einen Moniker, der die Kerberos-Authentifizierung mithilfe des Prinzipals "mydomain \\ server" anfordert.

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    Im gegensatz dazu zeigt das folgende Beispiel einen Moniker, der die NTLM-Authentifizierung mithilfe der Domäne "mydomain" anfordert.

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



