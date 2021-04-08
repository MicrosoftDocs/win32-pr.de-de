---
description: Sie können eine der folgenden Methoden verwenden, um den Dienst zu debuggen.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Debuggen eines Diensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750800"
---
# <a name="debugging-a-service"></a><span data-ttu-id="5f16b-103">Debuggen eines Diensts</span><span class="sxs-lookup"><span data-stu-id="5f16b-103">Debugging a Service</span></span>

<span data-ttu-id="5f16b-104">Sie können eine der folgenden Methoden verwenden, um den Dienst zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="5f16b-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="5f16b-105">Verwenden Sie den Debugger, um den Dienst zu debuggen, während er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f16b-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="5f16b-106">Rufen Sie zuerst die Prozess-ID (PID) des Dienst Prozesses ab.</span><span class="sxs-lookup"><span data-stu-id="5f16b-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="5f16b-107">Nachdem Sie die PID abgerufen haben, fügen Sie Sie an den laufenden Prozess an.</span><span class="sxs-lookup"><span data-stu-id="5f16b-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="5f16b-108">Syntax Informationen finden Sie in der Dokumentation, die in Ihrem Debugger enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5f16b-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="5f16b-109">Rufen Sie die [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) -Funktion auf, um den Debugger für Just-in-Time-Debugging aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5f16b-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="5f16b-110">Geben Sie einen Debugger an, der beim Starten eines Programms verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f16b-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="5f16b-111">Erstellen Sie hierzu einen Schlüssel mit dem Namen " **Bild Datei Ausführungs Optionen** " im folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="5f16b-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="5f16b-112">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="5f16b-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="5f16b-113">Erstellen Sie einen Unterschlüssel mit dem gleichen Namen wie Ihr Dienst (z. b. MYSERV.EXE).</span><span class="sxs-lookup"><span data-stu-id="5f16b-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="5f16b-114">Fügen Sie diesem Unterschlüssel einen Wert vom Typ **reg \_ SZ** namens **Debugger** hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f16b-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="5f16b-115">Verwenden Sie den vollständigen Pfad zum Debugger als Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="5f16b-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="5f16b-116">Wählen Sie im Applet System Steuerungs applet ihren Dienst aus, klicken Sie auf **Start** , und aktivieren Sie **die Option Dienst für die Interaktion mit dem Desktop zulassen**.</span><span class="sxs-lookup"><span data-stu-id="5f16b-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="5f16b-117">Der Dienst muss ein interaktiver Dienst sein, andernfalls kann der Debugger nicht auf dem Standard Desktop ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5f16b-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="5f16b-118">Beachten Sie, dass dieses Verfahren ab Windows Vista nicht mehr unterstützt wird, da alle Dienste in einer Sitzung ausgeführt werden, die ausschließlich für Dienste reserviert ist und die Anzeige einer Benutzeroberfläche nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f16b-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="5f16b-119">Verwenden Sie die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) zum Protokollieren von Informationen.</span><span class="sxs-lookup"><span data-stu-id="5f16b-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="5f16b-120">Um den Initialisierungs Code eines automatischen Start Diensts zu debuggen, müssen Sie den Dienst temporär installieren und ausführen, um einen Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="5f16b-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="5f16b-121">Manchmal kann es erforderlich sein, einen Dienst als Konsolenanwendung zu Debuggingzwecken auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5f16b-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="5f16b-122">In diesem Szenario gibt die Funktion " [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) " einen Fehler bei der **\_ \_ Dienst \_ Controller \_ Verbindung** zurück.</span><span class="sxs-lookup"><span data-stu-id="5f16b-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="5f16b-123">Stellen Sie daher sicher, dass Sie Ihren Code so strukturieren, dass er nicht aufgerufen wird, wenn dieser Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f16b-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f16b-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f16b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f16b-125">Debuggen einer Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="5f16b-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="5f16b-126">Debuggingtools für Windows</span><span class="sxs-lookup"><span data-stu-id="5f16b-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
