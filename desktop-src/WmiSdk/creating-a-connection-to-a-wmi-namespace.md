---
description: 'Nachdem Sie die Standard Aufrufe von com festgelegt haben, müssen Sie mithilfe eines Aufrufs der IWbemLocator:: ConnectServer-Methode eine Verbindung mit WMI herstellen.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Erstellen einer Verbindung mit einem WMI-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485742"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="d47a4-103">Erstellen einer Verbindung mit einem WMI-Namespace</span><span class="sxs-lookup"><span data-stu-id="d47a4-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="d47a4-104">Nachdem Sie die Standard Aufrufe von com festgelegt haben, müssen Sie mithilfe eines Aufrufs der [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode eine Verbindung mit WMI herstellen.</span><span class="sxs-lookup"><span data-stu-id="d47a4-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="d47a4-105">Die **ConnectServer** -Methode gibt einen Proxy einer [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="d47a4-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="d47a4-106">Mithilfe von **IWbemServices** können Sie auf die verschiedenen Funktionen von WMI zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d47a4-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="d47a4-107">Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="d47a4-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="d47a4-108">Im folgenden Verfahren wird beschrieben, wie eine Verbindung mit einem WMI-Namespace erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d47a4-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="d47a4-109">**So erstellen Sie eine Verbindung mit einem WMI-Namespace**</span><span class="sxs-lookup"><span data-stu-id="d47a4-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="d47a4-110">Initialisieren Sie die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle durch einen Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="d47a4-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="d47a4-111">Für WMI ist es nicht erforderlich, dass Sie beim Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)zusätzliche Prozeduren ausführen.</span><span class="sxs-lookup"><span data-stu-id="d47a4-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="d47a4-112">Im folgenden Codebeispiel wird die Initialisierung von [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d47a4-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   <span data-ttu-id="d47a4-113">Stellen Sie eine Verbindung mit WMI her, indem Sie die Methode [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) abrufen.</span><span class="sxs-lookup"><span data-stu-id="d47a4-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="d47a4-114">Die [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Methode gibt einen Proxy an eine [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle zurück, die verwendet, um auf den lokalen WMI-Namespace zuzugreifen, der in dem Aufrufen von **ConnectServer** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d47a4-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="d47a4-115">Im folgenden Codebeispiel wird das Abrufen von [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d47a4-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

<span data-ttu-id="d47a4-116">Nachdem Sie einen Zeiger auf den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy erhalten haben, müssen Sie die Sicherheit des Proxys für den Zugriff auf WMI festlegen.</span><span class="sxs-lookup"><span data-stu-id="d47a4-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="d47a4-117">Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d47a4-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d47a4-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d47a4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d47a4-119">Erstellen einer WMI-Anwendung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="d47a4-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="d47a4-120">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="d47a4-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
