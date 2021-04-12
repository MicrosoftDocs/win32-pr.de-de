---
title: Erstellen von SPNs für einen RpcNs-Dienst
description: Im folgenden Codebeispiel werden die Dienst Prinzipal Namen (SPNs) für einen RPC-Dienst verfasst, der über einen Eintrag im rpcservices-Container im-Verzeichnis verfügt. Ein RPC-Dienst verwendet die rpcnsbindingexport-Funktion, um den rpcservices-Eintrag zu erstellen.
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- Erstellen von SPNs für eine RpcNs-Dienst Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472652"
---
# <a name="composing-spns-for-an-rpcns-service"></a><span data-ttu-id="a0c35-105">Erstellen von SPNs für einen RpcNs-Dienst</span><span class="sxs-lookup"><span data-stu-id="a0c35-105">Composing SPNs for an RpcNs Service</span></span>

<span data-ttu-id="a0c35-106">Im folgenden Codebeispiel werden die Dienst Prinzipal Namen (SPNs) für einen RPC-Dienst verfasst, der über einen Eintrag im rpcservices-Container im-Verzeichnis verfügt.</span><span class="sxs-lookup"><span data-stu-id="a0c35-106">The following code example composes the service principal names (SPNs) for an RPC service that has an entry in the RpcServices container in the directory.</span></span> <span data-ttu-id="a0c35-107">Ein RPC-Dienst verwendet die [**rpcnsbindingexport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) -Funktion, um den rpcservices-Eintrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0c35-107">An RPC service uses the [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) function to create its RpcServices entry.</span></span>

<span data-ttu-id="a0c35-108">Ein RPC-Dienst verwendet dieses Codebeispiel, um den SPN oder SPNs zu erstellen, die eine Instanz des Dienstanbieter identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a0c35-108">An RPC service uses this code example to build the SPN or SPNs that identify an instance of the service.</span></span> <span data-ttu-id="a0c35-109">Der Dienst verwendet diese Routine, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="a0c35-109">The service uses this routine to perform the following tasks:</span></span>

-   <span data-ttu-id="a0c35-110">, Um die SPNs im Verzeichnis zu registrieren oder die Registrierung aufzuheben, wenn der Dienst installiert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a0c35-110">To register or unregister the SPNs in the directory, when the service is installed or removed.</span></span> <span data-ttu-id="a0c35-111">Weitere Informationen und ein Codebeispiel finden Sie unter [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="a0c35-111">For more information and a code example, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>
-   <span data-ttu-id="a0c35-112">Registrieren Sie sich beim Start des Dienstanbieter beim RPC-Authentifizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="a0c35-112">Register itself with the RPC authentication service when the service starts.</span></span> <span data-ttu-id="a0c35-113">Weitere Informationen finden Sie unter [gegenseitige Authentifizierung in RPC-Anwendungen](mutual-authentication-in-rpc-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a0c35-113">For more information, see [Mutual Authentication in RPC Applications](mutual-authentication-in-rpc-applications.md).</span></span>

<span data-ttu-id="a0c35-114">In diesem Codebeispiel wird der Distinguished Name des rpcservices-Eintrags des Diensts verwendet, um den SPN zu verfassen.</span><span class="sxs-lookup"><span data-stu-id="a0c35-114">This code example uses the distinguished name of the service's RpcServices entry to compose the SPN.</span></span> <span data-ttu-id="a0c35-115">Bevor Sie diesen Code aufrufen, rufen Sie die [**rpcnsbindingexport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) -Funktion auf, um den rpcservices-Eintrag des Diensts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0c35-115">Before calling this code, call the [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) function to create the service's RpcServices entry.</span></span>

<span data-ttu-id="a0c35-116">In diesem Codebeispiel wird die [**dsgetspn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) -Funktion aufgerufen, um einen SPN zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0c35-116">This code example calls the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to build an SPN.</span></span> <span data-ttu-id="a0c35-117">Der SPN besteht aus dem Dienst Klassennamen und dem Distinguished Name des Dienst-rpcservices-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="a0c35-117">The SPN is composed from service class name and the distinguished name of the service RpcServices entry.</span></span>


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 