---
description: Mit Windows 8 und Windows Server 2012 wird die Möglichkeit eingeführt, dass Software, die auf einem virtuellen Computer ausgeführt wird, erkennt, dass möglicherweise ein Zeit Verschiebungs Ereignis aufgetreten ist.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Generierungs Bezeichner der virtuellen Maschine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350076"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="f506b-103">Generierungs Bezeichner der virtuellen Maschine</span><span class="sxs-lookup"><span data-stu-id="f506b-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="f506b-104">Mit Windows 8 und Windows Server 2012 wird die Möglichkeit eingeführt, dass Software, die auf einem virtuellen Computer ausgeführt wird, erkennt, dass möglicherweise ein Zeit Verschiebungs Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f506b-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="f506b-105">Zeit Verschiebungs Ereignisse können aufgrund einer Anwendung einer Momentaufnahme eines virtuellen Computers oder der Wiederherstellung einer Sicherung virtueller Computer auftreten.</span><span class="sxs-lookup"><span data-stu-id="f506b-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="f506b-106">Weitere Informationen zu dieser Funktion finden Sie im Whitepaper zum Generieren der [virtuellen Maschine](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span><span class="sxs-lookup"><span data-stu-id="f506b-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f506b-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f506b-107">Prerequisites</span></span>

<span data-ttu-id="f506b-108">Um die VM-Generations-ID von einem virtuellen Computer aus zu verwenden, muss der virtuelle Computer den folgenden entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f506b-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="f506b-109">Der virtuelle Computer muss auf einem Hypervisor ausgeführt werden, der die Unterstützung für die Generierung von VM-Generierungs Bezeichners implementiert.</span><span class="sxs-lookup"><span data-stu-id="f506b-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="f506b-110">Derzeit sind dies die folgenden:</span><span class="sxs-lookup"><span data-stu-id="f506b-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="f506b-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f506b-111">Windows 8</span></span>
    -   <span data-ttu-id="f506b-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f506b-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="f506b-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="f506b-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="f506b-114">Auf dem virtuellen Computer muss ein Gast Betriebssystem ausgeführt werden, das die VM-Generations Kennung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f506b-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="f506b-115">Derzeit sind dies die folgenden:</span><span class="sxs-lookup"><span data-stu-id="f506b-115">Currently, these are the following.</span></span>

    <span data-ttu-id="f506b-116">Die folgenden Betriebssysteme verfügen über systemeigene Unterstützung für den Generierungs Bezeichner der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f506b-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="f506b-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f506b-117">Windows 8</span></span>
    -   <span data-ttu-id="f506b-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f506b-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="f506b-119">Der folgende Betrieb kann als Gast Betriebssystem verwendet werden, wenn die Hyper-V-Integrationsdienste von Windows 8 oder Windows Server 2012 installiert sind.</span><span class="sxs-lookup"><span data-stu-id="f506b-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="f506b-120">Windows Server 2008 R2 mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f506b-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="f506b-121">Windows 7 mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f506b-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="f506b-122">Windows Server 2008 mit Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="f506b-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="f506b-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f506b-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="f506b-124">Windows Server 2003 mit Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="f506b-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="f506b-125">Windows Vista mit Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="f506b-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="f506b-126">Windows XP mit Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="f506b-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="f506b-127">Abrufen des Generations Bezeichners für die virtuelle Maschine</span><span class="sxs-lookup"><span data-stu-id="f506b-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="f506b-128">Führen Sie die folgenden Schritte aus, um den Generierungs Bezeichner für die virtuelle Maschine Programm gesteuert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f506b-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="f506b-129">Folgendes muss mit Administrator-oder System Berechtigungen ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f506b-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="f506b-130">Schließen Sie die Header Datei "vmgenerationcounter. h" in Ihre APP ein.</span><span class="sxs-lookup"><span data-stu-id="f506b-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="f506b-131">Die Header Datei enthält die folgenden Definitionen:</span><span class="sxs-lookup"><span data-stu-id="f506b-131">The header file contains these definitions:</span></span>
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  <span data-ttu-id="f506b-132">Öffnen Sie ein Handle für die " \\ \\ . \\ Vmgenerationcounter "-Gerät, [**das die**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" Funktion "verwendet.</span><span class="sxs-lookup"><span data-stu-id="f506b-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="f506b-133">Alternativ können Sie den PNP-Manager verwenden, um den Geräteschnittstellen- **GUID \_ devinterface- \_ VM \_ gencounter** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f506b-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="f506b-134">Diese Objekte sind nicht vorhanden, wenn die APP nicht auf einem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f506b-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="f506b-135">Senden Sie den [**IOCTL- \_ vmgencounter- \_ Lese**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) Vorgang IOCTL an den Treiber, um den Generierungs Bezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f506b-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="f506b-136">Der [**IOCTL \_ vmgencounter- \_ Lese**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) -ioctl-Vorgang funktioniert in einem von zwei Modi: Abruf und *ereignisgesteuert*. </span><span class="sxs-lookup"><span data-stu-id="f506b-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="f506b-137">Um die IOCTL im Abruf Modus auszugeben, senden Sie ioctl mit einem Eingabepuffer der Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f506b-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="f506b-138">Als Reaktion darauf ruft der Treiber den aktuellen Generierungs Bezeichner ab, schreibt ihn in den Ausgabepuffer und schließt die IOCTL ab.</span><span class="sxs-lookup"><span data-stu-id="f506b-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="f506b-139">Um die IOCTL im ereignisbasierten Modus auszugeben, senden Sie die IOCTL mit einem Eingabepuffer, der einen vorhandenen Generations Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="f506b-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="f506b-140">Als Reaktion darauf wartet der Treiber, bis sich der aktuelle Generations Bezeichner von dem weiter gegebenen Generations Bezeichner unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="f506b-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="f506b-141">Wenn sich der Generierungs Bezeichner ändert, schreibt der Treiber den aktuellen Generierungs Bezeichner in den Ausgabepuffer und schließt die IOCTL ab.</span><span class="sxs-lookup"><span data-stu-id="f506b-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="f506b-142">In beiden Modi wird das Format und die Länge des Ausgabepuffers von der [**VM \_ gencounter**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) -Struktur vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="f506b-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="f506b-143">Der Abruf Modus wird von allen oben aufgeführten Gastbetriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f506b-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="f506b-144">Der Ereignis gestützte Modus wird nur unter Windows Vista mit SP2, Windows Server 2008 mit SP2 und neueren Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f506b-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="f506b-145">Unter früheren Betriebssystemen schlägt die IOCTL-Anweisung fehl, und der Fehlercode wird **\_ nicht \_ unterstützt** , wenn Sie im ereignisbasierten Modus ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f506b-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="f506b-146">Es ist möglich, dass sich der Generations Bezeichner zwischen dem vom Treiber abgerufenen Zeitpunkt und dem Zeitpunkt, zu dem die IOCTL abgeschlossen ist, ändert.</span><span class="sxs-lookup"><span data-stu-id="f506b-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="f506b-147">Dies kann dazu führen, dass die Client-App veraltete Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="f506b-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="f506b-148">Um dies zu vermeiden, kann die Client-App den ereignisbasierten Modus verwenden, um sicherzustellen, dass Sie schließlich alle Aktualisierungen des Generations Bezeichners erfährt.</span><span class="sxs-lookup"><span data-stu-id="f506b-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="f506b-149">Durch die Übernahme des aktuellen Bezeichners der Client-App als Eingabe vermeidet der Ereignis gesteuerter Modus potenzielle Racebedingungen, die dazu führen, dass der Aufrufer Benachrichtigungen verpasst.</span><span class="sxs-lookup"><span data-stu-id="f506b-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="f506b-150">Im folgenden Codebeispiel wird gezeigt, wie die obigen Aktionen zum Abrufen des Generations Bezeichners für die virtuelle Maschine durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f506b-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="f506b-151">Der folgende Code muss mit Administrator-oder System Berechtigungen ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f506b-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="f506b-152">Ermitteln, ob ein Zeit Verschiebungs Ereignis aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="f506b-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="f506b-153">Nachdem Sie den Generations Bezeichner für die virtuelle Maschine abgerufen haben, sollten Sie ihn zur späteren Verwendung speichern.</span><span class="sxs-lookup"><span data-stu-id="f506b-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="f506b-154">Bevor Ihre APP einen zeitabhängigen Vorgang durchführt (z. b. das Ausführen eines Commits für eine Datenbank), sollten Sie den Generierungs Bezeichner erneut abrufen und ihn mit dem gespeicherten Wert vergleichen.</span><span class="sxs-lookup"><span data-stu-id="f506b-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="f506b-155">Wenn sich der Bezeichner geändert hat, bedeutet dies, dass ein Zeit Verschiebungs Ereignis aufgetreten ist, und die APP muss entsprechend agieren.</span><span class="sxs-lookup"><span data-stu-id="f506b-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
