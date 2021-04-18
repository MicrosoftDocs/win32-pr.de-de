---
description: Ein untergeordneter Prozess kann Handles von seinem übergeordneten Prozess erben. Ein geerbtes Handle ist nur im Kontext des untergeordneten Prozesses gültig. Führen Sie die folgenden Schritte aus, um zu ermöglichen, dass ein untergeordneter Prozess geöffnete Handles von seinem übergeordneten Prozess erbt.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Behandlung von Vererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351053"
---
# <a name="handle-inheritance"></a><span data-ttu-id="909ba-105">Behandlung von Vererbung</span><span class="sxs-lookup"><span data-stu-id="909ba-105">Handle Inheritance</span></span>

<span data-ttu-id="909ba-106">Ein untergeordneter Prozess kann Handles von seinem übergeordneten Prozess erben.</span><span class="sxs-lookup"><span data-stu-id="909ba-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="909ba-107">Ein geerbtes Handle ist nur im Kontext des untergeordneten Prozesses gültig.</span><span class="sxs-lookup"><span data-stu-id="909ba-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="909ba-108">Führen Sie die folgenden Schritte aus, um zu ermöglichen, dass ein untergeordneter Prozess geöffnete Handles von seinem übergeordneten Prozess erbt.</span><span class="sxs-lookup"><span data-stu-id="909ba-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="909ba-109">Erstellen Sie das Handle mit dem **binherithandle** -Member der Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , die auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="909ba-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="909ba-110">Erstellen Sie den untergeordneten Prozess mithilfe der Funktion " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ", wobei der *binherithandles* -Parameter auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="909ba-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="909ba-111">Die [**duplialisierandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion dupliziert ein Handle, das im aktuellen Prozess oder in einem anderen Prozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="909ba-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="909ba-112">Wenn eine Anwendung eine ihrer Handles für einen anderen Prozess dupliziert, ist das doppelte Handle nur im Kontext des anderen Prozesses gültig.</span><span class="sxs-lookup"><span data-stu-id="909ba-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="909ba-113">Ein dupliziertes oder geerbtes Handle ist ein eindeutiger Wert, verweist jedoch auf dasselbe Objekt wie das ursprüngliche handle.</span><span class="sxs-lookup"><span data-stu-id="909ba-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="909ba-114">Prozesse können Handles für die folgenden Objekttypen erben oder duplizieren:</span><span class="sxs-lookup"><span data-stu-id="909ba-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="909ba-115">Access Token</span><span class="sxs-lookup"><span data-stu-id="909ba-115">Access Token</span></span>
-   <span data-ttu-id="909ba-116">Kommunikationsgerät</span><span class="sxs-lookup"><span data-stu-id="909ba-116">Communications device</span></span>
-   <span data-ttu-id="909ba-117">Konsolen Eingabe</span><span class="sxs-lookup"><span data-stu-id="909ba-117">Console input</span></span>
-   <span data-ttu-id="909ba-118">Bildschirm Puffer der Konsole</span><span class="sxs-lookup"><span data-stu-id="909ba-118">Console screen buffer</span></span>
-   <span data-ttu-id="909ba-119">Desktop</span><span class="sxs-lookup"><span data-stu-id="909ba-119">Desktop</span></span>
-   <span data-ttu-id="909ba-120">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="909ba-120">Directory</span></span>
-   <span data-ttu-id="909ba-121">Ereignis</span><span class="sxs-lookup"><span data-stu-id="909ba-121">Event</span></span>
-   <span data-ttu-id="909ba-122">File</span><span class="sxs-lookup"><span data-stu-id="909ba-122">File</span></span>
-   <span data-ttu-id="909ba-123">Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="909ba-123">File mapping</span></span>
-   <span data-ttu-id="909ba-124">Auftrag</span><span class="sxs-lookup"><span data-stu-id="909ba-124">Job</span></span>
-   <span data-ttu-id="909ba-125">Mailslot</span><span class="sxs-lookup"><span data-stu-id="909ba-125">Mailslot</span></span>
-   <span data-ttu-id="909ba-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="909ba-126">Mutex</span></span>
-   <span data-ttu-id="909ba-127">Pipe</span><span class="sxs-lookup"><span data-stu-id="909ba-127">Pipe</span></span>
-   <span data-ttu-id="909ba-128">Prozess</span><span class="sxs-lookup"><span data-stu-id="909ba-128">Process</span></span>
-   <span data-ttu-id="909ba-129">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="909ba-129">Registry key</span></span>
-   <span data-ttu-id="909ba-130">Semaphore</span><span class="sxs-lookup"><span data-stu-id="909ba-130">Semaphore</span></span>
-   <span data-ttu-id="909ba-131">Steckdose</span><span class="sxs-lookup"><span data-stu-id="909ba-131">Socket</span></span>
-   <span data-ttu-id="909ba-132">Thread</span><span class="sxs-lookup"><span data-stu-id="909ba-132">Thread</span></span>
-   <span data-ttu-id="909ba-133">Timer</span><span class="sxs-lookup"><span data-stu-id="909ba-133">Timer</span></span>
-   <span data-ttu-id="909ba-134">Fenster Station</span><span class="sxs-lookup"><span data-stu-id="909ba-134">Window station</span></span>

<span data-ttu-id="909ba-135">Alle anderen Objekte sind für den Prozess, der Sie erstellt hat, privat. Ihre Objekt Handles können nicht dupliziert oder geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="909ba-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="909ba-136">Weitere Informationen finden Sie unter [Vererbung](/windows/desktop/ProcThread/inheritance).</span><span class="sxs-lookup"><span data-stu-id="909ba-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
