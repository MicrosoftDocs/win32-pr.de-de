---
title: Verfassen von SPNs für einen RpcNs-Dienst
description: Im folgenden Codebeispiel werden die Dienstprinzipalnamen (SERVICE Principal Names, SPNs) für einen RPC-Dienst erstellt, der über einen Eintrag im RpcServices-Container im Verzeichnis verfügt. Ein RPC-Dienst verwendet die RpcNsBindingExport-Funktion, um seinen RpcServices-Eintrag zu erstellen.
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- Verfassen von SPNs für ein RPCNs-Dienst-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d3e8d0140c7bbc8dfa9b9232c0cce32a11813a348a619a1cf0fc80c15b194fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022257"
---
# <a name="composing-spns-for-an-rpcns-service"></a>Verfassen von SPNs für einen RpcNs-Dienst

Im folgenden Codebeispiel werden die Dienstprinzipalnamen (SERVICE Principal Names, SPNs) für einen RPC-Dienst erstellt, der über einen Eintrag im RpcServices-Container im Verzeichnis verfügt. Ein RPC-Dienst verwendet die [**RpcNsBindingExport-Funktion,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) um seinen RpcServices-Eintrag zu erstellen.

Ein RPC-Dienst verwendet dieses Codebeispiel, um den SPN oder die SPNs zu erstellen, die eine Instanz des Diensts identifizieren. Der Dienst verwendet diese Routine, um die folgenden Aufgaben auszuführen:

-   Zum Registrieren oder Aufheben der Registrierung der SPNs im Verzeichnis, wenn der Dienst installiert oder entfernt wird. Weitere Informationen und ein Codebeispiel finden Sie unter [Registrieren der SPNs für einen Dienst.](registering-the-spns-for-a-service.md)
-   Registrieren Sie sich selbst beim RPC-Authentifizierungsdienst, wenn der Dienst gestartet wird. Weitere Informationen finden Sie unter [Gegenseitige Authentifizierung in RPC-Anwendungen.](mutual-authentication-in-rpc-applications.md)

In diesem Codebeispiel wird der Distinguished Name des RpcServices-Eintrags des Diensts verwendet, um den SPN zu erstellen. Rufen Sie vor dem Aufrufen dieses Codes die [**RpcNsBindingExport-Funktion**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) auf, um den RpcServices-Eintrag des Diensts zu erstellen.

Dieses Codebeispiel ruft die [**DsGetSpn-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) auf, um einen SPN zu erstellen. Der SPN besteht aus dem Dienstklassennamen und dem Distinguished Name des RpcServices-Eintrags des Diensts.


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



 

 