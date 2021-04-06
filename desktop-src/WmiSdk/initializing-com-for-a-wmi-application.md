---
description: Der erste Schritt beim Herstellen einer Verbindung mit WMI ist das Einrichten der com-Aufrufe an CoInitializeEx und CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Initialisieren von com für eine WMI-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960797"
---
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="2ac0b-103">Initialisieren von com für eine WMI-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2ac0b-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="2ac0b-104">Der erste Schritt beim Herstellen einer Verbindung mit WMI ist das Einrichten der com-Aufrufe an [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="2ac0b-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="2ac0b-105">Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="2ac0b-106">Im folgenden Verfahren wird beschrieben, wie com aus einer Client Anwendung initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="2ac0b-107">**So initialisieren Sie com über eine Client Anwendung**</span><span class="sxs-lookup"><span data-stu-id="2ac0b-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="2ac0b-108">Initialisieren Sie com mit einem Aufrufen von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="2ac0b-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="2ac0b-109">Der Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) ist ein Standardverfahren zum Einrichten einer COM-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="2ac0b-110">Daher ist es für WMI nicht erforderlich, dass Sie beim Aufrufen von **CoInitializeEx** weitere Prozeduren beachten.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="2ac0b-111">Weitere Informationen finden Sie unter [com](../com/component-object-model--com--portal.md).</span><span class="sxs-lookup"><span data-stu-id="2ac0b-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="2ac0b-112">Im folgenden Codebeispiel wird beschrieben, wie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="2ac0b-113">Legen Sie die allgemeinen com-Sicherheitsstufen mit einem aufrufswert für die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="2ac0b-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ist eine Standardfunktion, die beim Einrichten einer COM-Schnittstelle für einen Prozess aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="2ac0b-115">**CoInitializeSecurity** wird aufgerufen, wenn Sie die Standard Sicherheitseinstellungen für die Authentifizierung, den Identitätswechsel oder den Authentifizierungsdienst für einen gesamten Prozess festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="2ac0b-116">Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="2ac0b-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="2ac0b-117">Wenn Sie die Sicherheit für einen bestimmten Proxy festlegen oder ändern möchten, müssen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="2ac0b-118">Verwenden Sie **CoSetProxyBlanket** , wenn Sie com-Sicherheit festlegen oder ändern müssen, wenn Sie in einem anderen Prozess ausgeführt werden, in dem Sie die Standard Sicherheitseinstellungen für die Authentifizierung, den Identitätswechsel oder den Authentifizierungsdienst nicht steuern können.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="2ac0b-119">Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md) und [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="2ac0b-120">WMI weist mehrere Sicherheitsprobleme auf, die Sie beim Programmieren einer WMI-Client Anwendung beachten sollten.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="2ac0b-121">Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="2ac0b-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="2ac0b-122">Im folgenden Codebeispiel wird beschrieben, wie [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen wird, um die com-Sicherheit für den Prozess festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

<span data-ttu-id="2ac0b-123">Nachdem Sie com initialisiert haben, besteht der nächste Schritt im Erstellen einer Verbindung mit einem WMI-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2ac0b-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="2ac0b-124">Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="2ac0b-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ac0b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ac0b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ac0b-126">Erstellen einer WMI-Anwendung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="2ac0b-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="2ac0b-127">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="2ac0b-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
