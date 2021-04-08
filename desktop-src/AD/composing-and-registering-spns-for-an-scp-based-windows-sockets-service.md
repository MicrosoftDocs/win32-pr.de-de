---
title: Erstellen und Registrieren von SPNs für den SCP-basierten Windows Sockets-Dienst
description: Im folgenden Codebeispiel wird gezeigt, wie Sie die SPNs für einen Dienst verfassen und registrieren. Rufen Sie diesen Code nach dem Aufrufen von CreateService und dem Erstellen des Dienst Verbindungs Punkts (Service Connection Point, SCP) von Ihrem Dienst Installationsprogramm auf.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- Dienst Prinzipal Namen AD, erstellen und Registrieren von SPNs für einen SCP-basierten Windows Sockets-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724617"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Erstellen und Registrieren von SPNs für den SCP-basierten Windows Sockets-Dienst

Im folgenden Codebeispiel wird gezeigt, wie Sie die SPNs für einen Dienst verfassen und registrieren. Rufen Sie diesen Code nach dem Aufrufen von [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) und dem Erstellen des Dienst Verbindungs Punkts (Service Connection Point, SCP) von Ihrem Dienst Installationsprogramm auf.

Im folgenden Codebeispiel werden die Funktionen **spncompose** und **spnregister** aufgerufen, um den SPN zu verfassen und zu registrieren. Weitere Informationen und den **spncompose** -Quellcode finden Sie unter Verfassen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md). Weitere Informationen und den **spnregister** -Quellcode finden Sie unter [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).

In diesem Beispiel werden der Dienst Klassenname und der Distinguished Name seines Dienst Prinzipals verwendet, um seinen Dienst Prinzipal Namen zu erstellen. Weitere Informationen und ein Codebeispiel, das zeigt, wie der Client an den Dienst-SCP gebunden wird, um diese namens Zeichenfolgen abzurufen, finden Sie unter [wie Clients einen Dienst Verbindungspunkt suchen und verwenden](how-clients-find-and-use-a-service-connection-point.md). Beachten Sie, dass der Code zum Erstellen eines SPN abhängig vom Diensttyp und den Mechanismen, die zum Veröffentlichen des diensdienstanbieter verwendet werden, abweicht.

Der Dienst registriert seinen SPN, indem er ihn im **servicePrincipalName** -Attribut des Dienst Konto Objekts im Verzeichnis speichert. Wenn der Dienst unter dem Konto "LocalSystem" statt unter einem Dienst Konto ausgeführt wird, registriert er seinen SPN unter dem Objekt des lokalen Computer Kontos im Verzeichnis.


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



Sie können ähnlichen Code verwenden, um die Registrierung Ihrer SPNs aufzuheben, wenn der Dienst deinstalliert wird. Geben Sie den DS-SPN-Vorgang zum **\_ Löschen von \_ \_ SPN \_** -SPN anstelle von **DS \_ SPN \_ Add \_ SPN \_ op** an.

 

 