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
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a><span data-ttu-id="6e0e3-105">Erstellen und Registrieren von SPNs für den SCP-basierten Windows Sockets-Dienst</span><span class="sxs-lookup"><span data-stu-id="6e0e3-105">Composing and registering SPNs for SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="6e0e3-106">Im folgenden Codebeispiel wird gezeigt, wie Sie die SPNs für einen Dienst verfassen und registrieren.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-106">The following code example shows how to compose and register the SPNs for a service.</span></span> <span data-ttu-id="6e0e3-107">Rufen Sie diesen Code nach dem Aufrufen von [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) und dem Erstellen des Dienst Verbindungs Punkts (Service Connection Point, SCP) von Ihrem Dienst Installationsprogramm auf.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-107">Call this code from your service installer after calling [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) and creating the service's service connection point (SCP).</span></span>

<span data-ttu-id="6e0e3-108">Im folgenden Codebeispiel werden die Funktionen **spncompose** und **spnregister** aufgerufen, um den SPN zu verfassen und zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-108">The following code example calls the **SpnCompose** and **SpnRegister** example functions that compose and register the SPN.</span></span> <span data-ttu-id="6e0e3-109">Weitere Informationen und den **spncompose** -Quellcode finden Sie unter Verfassen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="6e0e3-109">For more information and the **SpnCompose** source code, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="6e0e3-110">Weitere Informationen und den **spnregister** -Quellcode finden Sie unter [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="6e0e3-110">For more information and the **SpnRegister** source code, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="6e0e3-111">In diesem Beispiel werden der Dienst Klassenname und der Distinguished Name seines Dienst Prinzipals verwendet, um seinen Dienst Prinzipal Namen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-111">This example uses the service class name and the distinguished name of its SCP to create its service principal name.</span></span> <span data-ttu-id="6e0e3-112">Weitere Informationen und ein Codebeispiel, das zeigt, wie der Client an den Dienst-SCP gebunden wird, um diese namens Zeichenfolgen abzurufen, finden Sie unter [wie Clients einen Dienst Verbindungspunkt suchen und verwenden](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="6e0e3-112">For more information and a code example that shows how the client binds to the service SCP to retrieve these name strings, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="6e0e3-113">Beachten Sie, dass der Code zum Erstellen eines SPN abhängig vom Diensttyp und den Mechanismen, die zum Veröffentlichen des diensdienstanbieter verwendet werden, abweicht.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-113">Be aware that the code for composing an SPN varies depending on the type of service and the mechanisms used to publish the service.</span></span>

<span data-ttu-id="6e0e3-114">Der Dienst registriert seinen SPN, indem er ihn im **servicePrincipalName** -Attribut des Dienst Konto Objekts im Verzeichnis speichert.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-114">The service registers its SPN by storing it in the **servicePrincipalName** attribute of the service's account object in the directory.</span></span> <span data-ttu-id="6e0e3-115">Wenn der Dienst unter dem Konto "LocalSystem" statt unter einem Dienst Konto ausgeführt wird, registriert er seinen SPN unter dem Objekt des lokalen Computer Kontos im Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-115">If the service runs under the LocalSystem account instead of under a service account, it registers its SPN under the local computer account's object in the directory.</span></span>


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



<span data-ttu-id="6e0e3-116">Sie können ähnlichen Code verwenden, um die Registrierung Ihrer SPNs aufzuheben, wenn der Dienst deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-116">You can use similar code to unregister your SPNs when your service is uninstalled.</span></span> <span data-ttu-id="6e0e3-117">Geben Sie den DS-SPN-Vorgang zum **\_ Löschen von \_ \_ SPN \_** -SPN anstelle von **DS \_ SPN \_ Add \_ SPN \_ op** an.</span><span class="sxs-lookup"><span data-stu-id="6e0e3-117">Specify the **DS\_SPN\_DELETE\_SPN\_OP** operation instead of **DS\_SPN\_ADD\_SPN\_OP**.</span></span>

 

 