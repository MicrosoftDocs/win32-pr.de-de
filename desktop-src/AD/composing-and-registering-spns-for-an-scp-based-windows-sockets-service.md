---
title: Verfassen und Registrieren von SPNs für SCP-basierte Windows Sockets Service
description: Das folgende Codebeispiel zeigt, wie Sie die SPNs für einen Dienst erstellen und registrieren. Rufen Sie diesen Code von Ihrem Dienstinstallationsprogramm auf, nachdem Sie CreateService aufgerufen und den Dienstverbindungspunkt (Service Connection Point, SCP) des Diensts erstellt haben.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- Dienstprinzipalnamen AD, Verfassen und Registrieren von SPNs für einen SCP-basierten Windows Sockets-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e7724ef764b9269357ed932425c3526be4f7dc41a8640d29420cc48904c0f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022348"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Verfassen und Registrieren von SPNs für SCP-basierte Windows Sockets Service

Das folgende Codebeispiel zeigt, wie Sie die SPNs für einen Dienst erstellen und registrieren. Rufen Sie diesen Code von Ihrem Dienstinstallationsprogramm auf, nachdem [**Sie CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) aufgerufen und den Dienstverbindungspunkt (Service Connection Point, SCP) des Diensts erstellt haben.

Das folgende Codebeispiel ruft die **Beispielfunktionen SpnCompose** und **SpnRegister** auf, die den SPN zusammenstellen und registrieren. Weitere Informationen und den **SpnCompose-Quellcode** finden Sie unter [Zusammenstellen der SPNs für einen Dienst mit einem SCP.](composing-the-spns-for-a-service-with-an-scp.md) Weitere Informationen und den **SpnRegister-Quellcode** finden Sie unter [Registrieren der SPNs für einen Dienst.](registering-the-spns-for-a-service.md)

In diesem Beispiel werden der Dienstklassenname und der Distinguished Name des SCP verwendet, um den Dienstprinzipalnamen zu erstellen. Weitere Informationen und ein Codebeispiel, das zeigt, wie der Client an den Dienst-SCP gebunden wird, um diese Namenszeichenfolgen abzurufen, finden Sie unter [Suchen und Verwenden eines Dienstverbindungspunkts](how-clients-find-and-use-a-service-connection-point.md)durch Clients. Beachten Sie, dass der Code zum Verfassen eines SPN je nach Diensttyp und den Mechanismen zum Veröffentlichen des Diensts variiert.

Der Dienst registriert seinen SPN, indem er ihn im **servicePrincipalName-Attribut** des Kontoobjekts des Diensts im Verzeichnis speichert. Wenn der Dienst unter dem LocalSystem-Konto und nicht unter einem Dienstkonto ausgeführt wird, registriert er seinen SPN unter dem -Objekt des lokalen Computerkontos im Verzeichnis.


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



Sie können ähnlichen Code verwenden, um die Registrierung Ihrer SPNs bei der Deinstallation des Diensts zu aufheben. Geben Sie den **VORGANG DS \_ \_ SPN DELETE \_ SPN \_ OP** anstelle von **DS \_ SPN \_ ADD \_ SPN \_ OP** an.

 

 