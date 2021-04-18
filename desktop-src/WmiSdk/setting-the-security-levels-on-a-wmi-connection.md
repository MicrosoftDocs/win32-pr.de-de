---
description: Nachdem Sie einen Zeiger auf einen IWbemServices-Proxy abgerufen haben, müssen Sie die Sicherheit des Proxys für den Zugriff auf WMI über den Proxy festlegen.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Festlegen der Sicherheitsstufen für eine WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350933"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="3a758-103">Festlegen der Sicherheitsstufen für eine WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="3a758-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="3a758-104">Nachdem Sie einen Zeiger auf einen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy abgerufen haben, müssen Sie die Sicherheit des Proxys für den Zugriff auf WMI über den Proxy festlegen.</span><span class="sxs-lookup"><span data-stu-id="3a758-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="3a758-105">Sie müssen die Sicherheit festlegen, da der **IWbemServices** -Proxy Zugriff auf ein Out-of-Process-Objekt gewährt.</span><span class="sxs-lookup"><span data-stu-id="3a758-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="3a758-106">Im Allgemeinen lässt die com-Sicherheit nicht zu, dass ein Prozess auf einen anderen Prozess zugreift, wenn Sie die richtigen Sicherheitseigenschaften nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="3a758-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="3a758-107">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.</span><span class="sxs-lookup"><span data-stu-id="3a758-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="3a758-108">Verbindungen mit unterschiedlichen Betriebssystemen erfordern unterschiedliche Authentifizierungs Stufen und Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="3a758-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="3a758-109">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3a758-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="3a758-110">Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="3a758-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="3a758-111">Im folgenden Verfahren wird beschrieben, wie die Sicherheitsstufen für eine WMI-Verbindung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a758-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="3a758-112">**So legen Sie die Sicherheitsstufen für eine WMI-Verbindung fest**</span><span class="sxs-lookup"><span data-stu-id="3a758-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="3a758-113">Legen Sie die Sicherheitsstufen des [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxys mit einem Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)fest.</span><span class="sxs-lookup"><span data-stu-id="3a758-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="3a758-114">Im folgenden Codebeispiel wird eine gängige Methode zum Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3a758-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

<span data-ttu-id="3a758-115">Nachdem Sie die Sicherheitsstufen für Ihren [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3a758-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="3a758-116">Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie die Anwendung Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="3a758-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="3a758-117">Weitere Informationen finden Sie unter [Bereinigen und Herunterfahren einer WMI-Anwendung](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="3a758-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
