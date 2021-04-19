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
# <a name="virtual-machine-generation-identifier"></a>Generierungs Bezeichner der virtuellen Maschine

Mit Windows 8 und Windows Server 2012 wird die Möglichkeit eingeführt, dass Software, die auf einem virtuellen Computer ausgeführt wird, erkennt, dass möglicherweise ein Zeit Verschiebungs Ereignis aufgetreten ist. Zeit Verschiebungs Ereignisse können aufgrund einer Anwendung einer Momentaufnahme eines virtuellen Computers oder der Wiederherstellung einer Sicherung virtueller Computer auftreten. Weitere Informationen zu dieser Funktion finden Sie im Whitepaper zum Generieren der [virtuellen Maschine](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).

## <a name="prerequisites"></a>Voraussetzungen

Um die VM-Generations-ID von einem virtuellen Computer aus zu verwenden, muss der virtuelle Computer den folgenden entsprechen.

-   Der virtuelle Computer muss auf einem Hypervisor ausgeführt werden, der die Unterstützung für die Generierung von VM-Generierungs Bezeichners implementiert. Derzeit sind dies die folgenden:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   Auf dem virtuellen Computer muss ein Gast Betriebssystem ausgeführt werden, das die VM-Generations Kennung unterstützt. Derzeit sind dies die folgenden:

    Die folgenden Betriebssysteme verfügen über systemeigene Unterstützung für den Generierungs Bezeichner der virtuellen Maschine.

    -   Windows 8
    -   Windows Server 2012
    -   

    Der folgende Betrieb kann als Gast Betriebssystem verwendet werden, wenn die Hyper-V-Integrationsdienste von Windows 8 oder Windows Server 2012 installiert sind.

    -   Windows Server 2008 R2 mit Service Pack 1 (SP1)
    -   Windows 7 mit Service Pack 1 (SP1)
    -   Windows Server 2008 mit Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 mit Service Pack 2 (SP2)
    -   Windows Vista mit Service Pack 2 (SP2)
    -   Windows XP mit Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Abrufen des Generations Bezeichners für die virtuelle Maschine

Führen Sie die folgenden Schritte aus, um den Generierungs Bezeichner für die virtuelle Maschine Programm gesteuert abzurufen.

> [!Note]  
> Folgendes muss mit Administrator-oder System Berechtigungen ausgeführt werden, um ordnungsgemäß zu funktionieren.

 

1.  Schließen Sie die Header Datei "vmgenerationcounter. h" in Ihre APP ein. Die Header Datei enthält die folgenden Definitionen:
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

    

2.  Öffnen Sie ein Handle für die " \\ \\ . \\ Vmgenerationcounter "-Gerät, [**das die**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" Funktion "verwendet. Alternativ können Sie den PNP-Manager verwenden, um den Geräteschnittstellen- **GUID \_ devinterface- \_ VM \_ gencounter** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}) zu verwenden. Diese Objekte sind nicht vorhanden, wenn die APP nicht auf einem virtuellen Computer ausgeführt wird.
3.  Senden Sie den [**IOCTL- \_ vmgencounter- \_ Lese**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) Vorgang IOCTL an den Treiber, um den Generierungs Bezeichner abzurufen.

    Der [**IOCTL \_ vmgencounter- \_ Lese**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) -ioctl-Vorgang funktioniert in einem von zwei Modi: Abruf und *ereignisgesteuert*. 

    Um die IOCTL im Abruf Modus auszugeben, senden Sie ioctl mit einem Eingabepuffer der Länge 0 (null). Als Reaktion darauf ruft der Treiber den aktuellen Generierungs Bezeichner ab, schreibt ihn in den Ausgabepuffer und schließt die IOCTL ab.

    Um die IOCTL im ereignisbasierten Modus auszugeben, senden Sie die IOCTL mit einem Eingabepuffer, der einen vorhandenen Generations Bezeichner enthält. Als Reaktion darauf wartet der Treiber, bis sich der aktuelle Generations Bezeichner von dem weiter gegebenen Generations Bezeichner unterscheidet. Wenn sich der Generierungs Bezeichner ändert, schreibt der Treiber den aktuellen Generierungs Bezeichner in den Ausgabepuffer und schließt die IOCTL ab.

    In beiden Modi wird das Format und die Länge des Ausgabepuffers von der [**VM \_ gencounter**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) -Struktur vorgegeben.

    Der Abruf Modus wird von allen oben aufgeführten Gastbetriebssystemen unterstützt. Der Ereignis gestützte Modus wird nur unter Windows Vista mit SP2, Windows Server 2008 mit SP2 und neueren Betriebssystemen unterstützt. Unter früheren Betriebssystemen schlägt die IOCTL-Anweisung fehl, und der Fehlercode wird **\_ nicht \_ unterstützt** , wenn Sie im ereignisbasierten Modus ausgegeben wird.

    Es ist möglich, dass sich der Generations Bezeichner zwischen dem vom Treiber abgerufenen Zeitpunkt und dem Zeitpunkt, zu dem die IOCTL abgeschlossen ist, ändert. Dies kann dazu führen, dass die Client-App veraltete Daten empfängt. Um dies zu vermeiden, kann die Client-App den ereignisbasierten Modus verwenden, um sicherzustellen, dass Sie schließlich alle Aktualisierungen des Generations Bezeichners erfährt. Durch die Übernahme des aktuellen Bezeichners der Client-App als Eingabe vermeidet der Ereignis gesteuerter Modus potenzielle Racebedingungen, die dazu führen, dass der Aufrufer Benachrichtigungen verpasst.

Im folgenden Codebeispiel wird gezeigt, wie die obigen Aktionen zum Abrufen des Generations Bezeichners für die virtuelle Maschine durchgeführt werden.

> [!Note]  
> Der folgende Code muss mit Administrator-oder System Berechtigungen ausgeführt werden, um ordnungsgemäß zu funktionieren.

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Ermitteln, ob ein Zeit Verschiebungs Ereignis aufgetreten ist

Nachdem Sie den Generations Bezeichner für die virtuelle Maschine abgerufen haben, sollten Sie ihn zur späteren Verwendung speichern. Bevor Ihre APP einen zeitabhängigen Vorgang durchführt (z. b. das Ausführen eines Commits für eine Datenbank), sollten Sie den Generierungs Bezeichner erneut abrufen und ihn mit dem gespeicherten Wert vergleichen. Wenn sich der Bezeichner geändert hat, bedeutet dies, dass ein Zeit Verschiebungs Ereignis aufgetreten ist, und die APP muss entsprechend agieren.

 

 
