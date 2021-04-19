---
description: Beim Zugriff auf einen Windows-Verwaltungsinstrumentation (WMI)-Server mit einem Skript können Sie zwischen NT LAN Manager (NTLM)-oder Kerberos-Authentifizierungs Protokollen wählen.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353971"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript

Beim Zugriff auf einen Windows-Verwaltungsinstrumentation (WMI)-Server mit einem Skript können Sie zwischen NT LAN Manager (NTLM)-oder Kerberos-Authentifizierungs Protokollen wählen. Die Angabe von Kerberos ist nicht erforderlich, außer bei der Verwendung der Delegierung. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit einer dritten Computer Delegierung](connecting-to-a-3rd-computer-delegation.md).

Da sich die Betriebssystemversionen von dem verwendeten Authentifizierungsdienst unterscheiden, wird empfohlen, beim Herstellen einer Verbindung mit einem Remote System keinen Wert für das Feld "Authority" anzugeben. Verwenden Sie stattdessen das Betriebssystem und die verteilte Version von Component Object Model (DCOM), um NTLM oder Kerberos auszuwählen. Wenn ein Authentifizierungsdienst angegeben wird, ist für die Syntax der Server Prinzipal Name erforderlich. Dies ist der Name des Ziel Computers anstelle des Domänen Controllers.

Sie können den Authority-Parameter nur mit Verbindungen mit Remote-WMI-Servern verwenden. Beim Verbindungsversuch tritt ein Fehler auf, wenn Sie versuchen, Autorisierungs Ebenen als Teil eines Monikers oder durch einen Aufruf von " [**Swap-Locator. ConnectServer**](swbemlocator-connectserver.md) " für eine lokale Verbindung festzulegen.

Führen Sie das folgende Verfahren aus, um den Authentifizierungsdienst anzugeben, den Sie im Parameter " *stranauthority* " der Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " oder der [Monikerzeichenfolge](constructing-a-moniker-string.md) verwenden möchten.

**So geben Sie die NTLM-oder Kerberos-Authentifizierung mit der Skript-API für WMI an**

1.  Wenn der Parameter " *stranauthority* " mit der Zeichenfolge "Kerberos:" beginnt, geht WMI davon aus, dass die Zeichenfolge auf einen Kerberos-Prinzipal Namen verweist und die Kerberos-Authentifizierung verwendet wird. Wenn der Parameter " *strauauthority* " mit der Zeichenfolge "ntlmdomain:" beginnt, verwendet WMI stattdessen die NTLM-Authentifizierung.
2.  Alternativ können Sie den Authority-Teil eines Monikers verwenden, um den Authentifizierungstyp anzugeben, der zum Herstellen der Verbindung mit WMI verwendet wird. Wenn Sie die Kerberos-Authentifizierung verwenden möchten, wenn Sie einen Moniker verwenden, schließen Sie die Zeichenfolge "Authority = Kerberos:" gefolgt vom Prinzipal Namen ein. Um die NTLM-Authentifizierung zu verwenden, schließen Sie die Zeichenfolge "Authority = ntlmdomain:" gefolgt vom NTLM-Domänen Namen ein.

    Das folgende Beispiel zeigt einen Moniker, der die Kerberos-Authentifizierung mit dem Prinzipal "mydomain \\ Server" anfordert.

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    Im Gegensatz dazu zeigt das folgende Beispiel einen Moniker, der die NTLM-Authentifizierung mithilfe der Domäne "mydomain" anfordert.

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



