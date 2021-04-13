---
title: Run-Time verknüpfen mit Wtsapi32.dll
description: Die Anwendung kann die Remotedesktopdienste-API verwenden, um zur Laufzeit dynamisch mit der Wtsapi32.dll zu verknüpfen. Zu diesem Zweck sollte die Anwendung die LoadLibrary-Funktion zum Laden Wtsapi32.dll abrufen.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390710"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="7804e-104">Run-Time verknüpfen mit Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="7804e-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="7804e-105">Wenn Ihre Anwendung in einer Umgebung ausgeführt wird, die keine Remotedesktopdienste Umgebung ist, aber Sie möchten, dass Ihre Anwendung zusätzliche Funktionen bereitstellt, wenn Sie in einer Remotedesktopdienste Umgebung ausgeführt wird, kann die Anwendung die Remotedesktopdienste-API verwenden, um die zusätzlichen Funktionen zu implementieren, und zur Laufzeit dynamisch mit der Wtsapi32.dll verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7804e-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="7804e-106">Zu diesem Zweck sollte die Anwendung die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion zum Laden Wtsapi32.dll abrufen.</span><span class="sxs-lookup"><span data-stu-id="7804e-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="7804e-107">Wenn der **LoadLibrary** -Rückruf fehlschlägt, kann die Anwendung mit der grundlegenden Funktionalität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7804e-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="7804e-108">Wenn **LoadLibrary** erfolgreich ist, kann die Anwendung die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen, um Zeiger auf die Remotedesktopdienste Funktionen abzurufen, die Sie aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="7804e-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="7804e-109">Wenn Ihre Anwendung nur für eine Remotedesktopdienste Umgebung vorgesehen ist, ist die dynamische Verknüpfung nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7804e-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="7804e-110">In diesem Fall können Sie Wtsapi32. h einschließen und mit Wtsapi32. lib verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7804e-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="7804e-111">Wenn Ihre Anwendung in einer anderen Umgebung als Remotedesktopdienste gestartet wird, wird Sie beendet, da Wtsapi32.dll nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7804e-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="7804e-112">Informationen zum bestimmen, ob Ihre Anwendung in einer Remotedesktopdienste-Umgebung ausgeführt wird, finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7804e-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7804e-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7804e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7804e-114">Allgemeine Programmier Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7804e-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 