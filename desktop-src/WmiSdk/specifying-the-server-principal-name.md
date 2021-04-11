---
description: Der Kerberos-Authentifizierungsdienst gibt den Server Prinzipal Namen an, um die Identität des Computers sicherzustellen, mit dem die Verbindung hergestellt wird.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Angeben des Server Prinzipal namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131004"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="f0054-103">Angeben des Server Prinzipal namens</span><span class="sxs-lookup"><span data-stu-id="f0054-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="f0054-104">Der Kerberos-Authentifizierungsdienst gibt den Server Prinzipal Namen an, um die Identität des Computers sicherzustellen, mit dem die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f0054-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="f0054-105">Geben Sie den Server Prinzipal Namen im aufzurufenden Skript für die Skript Methode " [**taubemlocator. ConnectServer**](swbemlocator-connectserver.md) " an, indem Sie den Namen des Remote Computers eingeben.</span><span class="sxs-lookup"><span data-stu-id="f0054-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="f0054-106">Geben Sie in C++ den Server Prinzipal Namen im *pserverprincname* -Parameter an, wenn Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) für den Proxy aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f0054-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="f0054-107">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f0054-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="f0054-108">Dieser Parameter ist für Kerberos erforderlich, um die gegenseitige Authentifizierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f0054-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="f0054-109">Allerdings lässt die Verwendung des standardmäßigen Server Prinzipal namens keine gegenseitige Authentifizierung zu.</span><span class="sxs-lookup"><span data-stu-id="f0054-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="f0054-110">Clients, für die die gegenseitige Authentifizierung wichtig ist, müssen einen Server Prinzipal Namen angeben, der mit der Server Identität übereinstimmt, die vom WMI-Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0054-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="f0054-111">Weitere Informationen zum Festlegen der Proxy Sicherheit und ein C++-Beispiel, das zeigt, wie der Server Prinzipal Name festgelegt wird, finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.</span><span class="sxs-lookup"><span data-stu-id="f0054-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="f0054-112">Weitere Informationen zum Festlegen des Server Prinzipal namens im Skript und Visual Basic finden Sie unter "WS- [**Locator. ConnectServer**](swbemlocator-connectserver.md) " und [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f0054-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="f0054-113">Im Gegensatz zu den meisten Sicherheitsprotokollen für Windows-Verwaltungsinstrumentation (WMI) und Component Object Model (com) können Sie den Server Prinzipal nicht in einem [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)-aufrufswert festlegen.</span><span class="sxs-lookup"><span data-stu-id="f0054-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f0054-114">Sie können jedoch den Server Prinzipal mit dem *bstrauauthority* -Parameter für [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)oder dem *pserverprincname* -Parameter für [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)festlegen.</span><span class="sxs-lookup"><span data-stu-id="f0054-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="f0054-115">Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="f0054-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="f0054-116">Im folgenden Codebeispiel wird gezeigt, wie der Server Prinzipal Name mit [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f0054-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a><span data-ttu-id="f0054-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0054-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0054-118">Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="f0054-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="f0054-119">Festlegen der Authentifizierung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="f0054-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="f0054-120">Festlegen der Sicherheit für IWbemServices und andere Proxys</span><span class="sxs-lookup"><span data-stu-id="f0054-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
