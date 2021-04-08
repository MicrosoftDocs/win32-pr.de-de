---
description: Nachdem Sie die Sicherheitsstufen für Ihren IWbemServices-Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen. Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie die Anwendung Herunterfahren.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Bereinigen und Herunterfahren einer WMI-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960223"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="f32ff-104">Bereinigen und Herunterfahren einer WMI-Anwendung</span><span class="sxs-lookup"><span data-stu-id="f32ff-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="f32ff-105">Nachdem Sie die Sicherheitsstufen für Ihren [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger festgelegt haben, können Sie auf die verschiedenen Funktionen von WMI zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f32ff-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="f32ff-106">Nachdem Sie die Verwendung von WMI abgeschlossen haben, müssen Sie die Anwendung Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="f32ff-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="f32ff-107">Im folgenden Verfahren wird beschrieben, wie Sie eine WMI-Anwendung bereinigen und Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="f32ff-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="f32ff-108">**So können Sie eine WMI-Anwendung bereinigen und Herunterfahren**</span><span class="sxs-lookup"><span data-stu-id="f32ff-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="f32ff-109">Freigeben beliebiger offener com-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f32ff-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="f32ff-110">Die beiden primären Schnittstellen, die Sie sich merken müssen, sind [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) und [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="f32ff-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="f32ff-111">[**CallInitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)aufruft.</span><span class="sxs-lookup"><span data-stu-id="f32ff-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="f32ff-112">Wie bei allen com-Anwendungen müssen Sie " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " am Ende der Anwendung anfügen.</span><span class="sxs-lookup"><span data-stu-id="f32ff-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="f32ff-113">Beenden Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f32ff-113">Exit your application.</span></span>

    <span data-ttu-id="f32ff-114">Im folgenden Codebeispiel wird gezeigt, wie eine WMI-Client Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f32ff-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="f32ff-115">Die `pSvc` Variable ist vom Typ [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* , und die ploc-Variable ist vom Typ [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .</span><span class="sxs-lookup"><span data-stu-id="f32ff-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="f32ff-116">Sie haben nun erfolgreich com initialisiert, auf WMI zugegriffen und die Anwendung beendet.</span><span class="sxs-lookup"><span data-stu-id="f32ff-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="f32ff-117">Weitere Informationen finden Sie unter [Beispiel: Erstellen einer WMI-Anwendung](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="f32ff-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f32ff-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f32ff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f32ff-119">Erstellen einer WMI-Anwendung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="f32ff-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
