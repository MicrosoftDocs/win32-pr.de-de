---
description: 'Eine der Hauptaufgaben von IWbemLocator:: ConnectServer für WMI ist die Rückgabe eines Zeigers auf einen IWbemServices-Proxy.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Festlegen der Authentifizierung mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349518"
---
# <a name="setting-authentication-using-c"></a><span data-ttu-id="6c895-103">Festlegen der Authentifizierung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="6c895-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="6c895-104">Eine der Hauptaufgaben von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) für WMI ist die Rückgabe eines Zeigers auf einen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy.</span><span class="sxs-lookup"><span data-stu-id="6c895-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="6c895-105">Über den **IWbemServices** -Proxy können Sie auf die Funktionen der WMI-Infrastruktur zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6c895-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="6c895-106">Der Zeiger auf den **IWbemServices** -Proxy hat jedoch die Identität des Client Anwendungsprozesses und nicht die Identität des **IWbemServices** -Prozesses.</span><span class="sxs-lookup"><span data-stu-id="6c895-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="6c895-107">Wenn Sie also versuchen, mit dem-Zeiger auf **IWbemServices** zuzugreifen, können Sie einen Zugriff verweigerten Code wie z. b. " **E \_ AccessDenied**" erhalten.</span><span class="sxs-lookup"><span data-stu-id="6c895-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="6c895-108">Um den Fehler "Zugriff verweigert" zu vermeiden, müssen Sie die Identität des neuen Zeigers mit einem Aufrufen der [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) -Schnittstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="6c895-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="6c895-109">Ein Anbieter kann die Sicherheit für einen Namespace so festlegen, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden den Paket Datenschutz (**PKTPRIVACY**) in der Verbindung mit diesem Namespace.</span><span class="sxs-lookup"><span data-stu-id="6c895-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="6c895-110">Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="6c895-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="6c895-111">Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, erhalten Sie die Meldung "Zugriff verweigert".</span><span class="sxs-lookup"><span data-stu-id="6c895-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="6c895-112">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="6c895-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="6c895-113">Weitere Informationen zum Festlegen der Authentifizierung bei der Skripterstellung finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="6c895-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="6c895-114">Festlegen der Sicherheit für eine IUnknown-Remote Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6c895-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="6c895-115">In einigen Situationen ist mehr Zugriff auf einen Server als nur ein Zeiger auf einen Proxy erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c895-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="6c895-116">Manchmal müssen Sie möglicherweise eine sichere Verbindung mit der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Proxys herstellen.</span><span class="sxs-lookup"><span data-stu-id="6c895-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="6c895-117">Mithilfe von **IUnknown** können Sie das Remote System nach Schnittstellen und anderen notwendigen Techniken Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6c895-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="6c895-118">Wenn sich ein Proxy auf einem Remote Computer befindet, delegiert der Server alle Aufrufe an die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Proxys an die **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6c895-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="6c895-119">Wenn Sie z. b. [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf einem Proxy aufzurufen und die angeforderte Schnittstelle nicht Teil des Proxys ist, sendet der Proxy den-Aufrufe an den Remote Server.</span><span class="sxs-lookup"><span data-stu-id="6c895-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="6c895-120">Der Remote Server überprüft wiederum die entsprechende Schnittstellen Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="6c895-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="6c895-121">Wenn der Server die-Schnittstelle unterstützt, Marshalls com einen neuen Proxy zurück an den Client, damit die Anwendung die neue-Schnittstelle verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6c895-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="6c895-122">Es treten Probleme auf, wenn der Client keine Zugriffsberechtigungen für den Remote Server hat, sondern die Anmelde Informationen eines Benutzers verwendet, der das verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c895-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="6c895-123">In dieser Situation tritt beim Versuch, auf die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf dem Remote Server zuzugreifen, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6c895-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="6c895-124">Die endgültige Version des Proxys schlägt ebenfalls fehl, da der aktuelle Benutzer keinen Zugriff auf den Remote Server hat.</span><span class="sxs-lookup"><span data-stu-id="6c895-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="6c895-125">Ein Symptom hierfür ist eine Verzögerung von einem oder zwei Sekunden, bevor die Client Anwendung die endgültige Proxy Version misslingt.</span><span class="sxs-lookup"><span data-stu-id="6c895-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="6c895-126">Der Fehler tritt auf, weil com versucht hat, unter Verwendung der Standard Sicherheitseinstellungen des aktuellen Benutzers auf den Remote Server zuzugreifen, die nicht die geänderten Anmelde Informationen enthalten, die den Zugriff auf den Server an erster Stelle zugelassen haben.</span><span class="sxs-lookup"><span data-stu-id="6c895-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="6c895-127">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.</span><span class="sxs-lookup"><span data-stu-id="6c895-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="6c895-128">Um die fehlgeschlagene Verbindung zu vermeiden, legen Sie mit [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) die Sicherheits Authentifizierung für den von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)zurückgegebenen Zeiger explizit fest.</span><span class="sxs-lookup"><span data-stu-id="6c895-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="6c895-129">Mithilfe von **CoSetProxyBlanket** können Sie sicherstellen, dass der Remote Server die richtige Authentifizierungs Identität erhält.</span><span class="sxs-lookup"><span data-stu-id="6c895-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="6c895-130">Im folgenden Codebeispiel wird gezeigt, wie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) verwendet wird, um auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Remote Schnittstelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6c895-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> <span data-ttu-id="6c895-131">Wenn Sie die Sicherheit für die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle eines Proxys festlegen, erstellt com eine Kopie des Proxys, die nicht freigegeben werden kann, bis Sie die [**entiinitialisierung**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)aufruft.</span><span class="sxs-lookup"><span data-stu-id="6c895-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6c895-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c895-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c895-133">Festlegen der Authentifizierung in WMI</span><span class="sxs-lookup"><span data-stu-id="6c895-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
