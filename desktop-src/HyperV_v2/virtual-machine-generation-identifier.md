---
description: Windows 8 und Windows Server 2012 können Software, die auf einem virtuellen Computer ausgeführt wird, erkennen, dass möglicherweise ein Zeitverschiebungsereignis aufgetreten ist.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Generierungsbezeichner für virtuelle Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d810a1a65e95f4dde0ccf9779b1e955f2630623e362ffbf94ab8ca36d51d116e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899010"
---
# <a name="virtual-machine-generation-identifier"></a>Generierungsbezeichner für virtuelle Computer

Windows 8 und Windows Server 2012 können Software, die auf einem virtuellen Computer ausgeführt wird, erkennen, dass möglicherweise ein Zeitverschiebungsereignis aufgetreten ist. Zeitverschiebungsereignisse können als Ergebnis einer Anwendung einer Momentaufnahme eines virtuellen Computers oder der Wiederherstellung einer Sicherung eines virtuellen Computers auftreten. Weitere Informationen zu dieser Funktionalität finden Sie im [Whitepaper Virtual Machine Generation ID (VM-Generations-ID).](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx)

## <a name="prerequisites"></a>Voraussetzungen

Um den Generierungsbezeichner des virtuellen Computers innerhalb eines virtuellen Computers zu verwenden, muss Ihr virtueller Computer folgende Anforderungen erfüllen.

-   Der virtuelle Computer muss auf einem Hypervisor ausgeführt werden, der Unterstützung für Generierungsbezeichner virtueller Computer implementiert. Derzeit sind dies die folgenden:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   Auf dem virtuellen Computer muss ein Gastbetriebssystem ausgeführt werden, das über Unterstützung für den Generierungsbezeichner des virtuellen Computers verfügt. Derzeit sind dies die folgenden.

    Die folgenden Betriebssysteme verfügen über native Unterstützung für den Generierungsbezeichner des virtuellen Computers.

    -   Windows 8
    -   Windows Server 2012
    -   

    Der folgende Betriebssystem kann als Gastbetriebssystem verwendet werden, wenn die Hyper-V-Integrationsdienste aus Windows 8 oder Windows Server 2012 installiert sind.

    -   Windows Server 2008 R2 mit Service Pack 1 (SP1)
    -   Windows 7 mit Service Pack 1 (SP1)
    -   Windows Server 2008 mit Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 mit Service Pack 2 (SP2)
    -   Windows Vista mit Service Pack 2 (SP2)
    -   Windows XP mit Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Abrufen des Generierungsbezeichners des virtuellen Computers

Führen Sie die folgenden Schritte aus, um den Generierungsbezeichner des virtuellen Computers programmgesteuert abzurufen.

> [!Note]  
> Folgendes muss mit Administrator- oder Systemberechtigungen ausgeführt werden, um ordnungsgemäß zu funktionieren.

 

1.  Schließen Sie die Headerdatei "vmgenerationcounter.h" in Ihre App ein. Die Headerdatei enthält die folgenden Definitionen:
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

    

2.  Öffnen Sie ein Handle für den \\ \\ . \\ VmGenerationCounter"-Gerät mithilfe der [**CreateFile-Funktion.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Alternativ können Sie den PnP-Manager verwenden, um die **Geräteschnittstellen-GUID \_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}) zu nutzen. Diese Objekte sind nicht vorhanden, wenn die App nicht auf einem virtuellen Computer ausgeführt wird.
3.  Senden Sie [**IOCTL \_ VMGENCOUNTER \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL an den Treiber, um den Generierungsbezeichner abzurufen.

    Die [**IOCTL-VMGENCOUNTER \_ READ-IOCTL \_**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) wird in einem von zwei Modi betrieben: *abruft* und *ereignisgesteuert.*

    Um die IOCTL im Abrufmodus auszugeben, übermitteln Sie die IOCTL mit einem Eingabepuffer der Länge 0 (null). Als Reaktion darauf ruft der Treiber den aktuellen Generationsbezeichner ab, schreibt ihn in den Ausgabepuffer und schließt die IOCTL ab.

    Um die IOCTL im ereignisgesteuerten Modus auszugeben, übermitteln Sie die IOCTL mit einem Eingabepuffer, der einen vorhandenen Generierungsbezeichner enthält. Als Reaktion darauf wartet der Treiber, bis sich der aktuelle Generierungsbezeichner von dem übergebenen Generierungsbezeichner unterscheidet. Wenn sich der Generierungsbezeichner ändert, schreibt der Treiber den aktuellen Generierungsbezeichner in den Ausgabepuffer und schließt die IOCTL ab.

    In beiden Modi wird das Format und die Länge des Ausgabepuffers durch die [**VM \_ GENCOUNTER-Struktur**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) vorgegeben.

    Der Abrufmodus wird für alle oben aufgeführten Gastbetriebssysteme unterstützt. Der ereignisgesteuerte Modus wird nur unter Windows Vista mit SP2, Windows Server 2008 mit SP2 und höher unterstützt. Unter früheren Betriebssystemen schlägt die IOCTL mit dem Fehlercode **ERROR \_ NOT \_ SUPPORTED** fehl, wenn sie im ereignisgesteuerten Modus ausgegeben wird.

    Es ist möglich, dass sich der Generierungsbezeichner zwischen dem Zeitpunkt, zu dem er vom Treiber abgerufen wird, und dem Zeitpunkt, zu dem die IOCTL abgeschlossen ist, ändert. Dies kann dazu führen, dass die Client-App veraltete Daten empfängt. Um dies zu vermeiden, kann die Client-App den ereignisgesteuerten Modus verwenden, um sicherzustellen, dass sie letztendlich über Updates des Generierungsbezeichners informiert wird. Indem der aktuelle Bezeichner der Client-App als Eingabe verwendet wird, vermeidet der ereignisgesteuerte Modus potenzielle Racebedingungen, die dazu führen würden, dass der Aufrufer Benachrichtigungen auslassen würde.

Das folgende Codebeispiel zeigt, wie die oben genannten Aktionen ausgeführt werden, um den Generierungsbezeichner des virtuellen Computers abzurufen.

> [!Note]  
> Der folgende Code muss mit Administrator- oder Systemberechtigungen ausgeführt werden, damit er ordnungsgemäß funktioniert.

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Bestimmen, ob ein Zeitverschiebungsereignis aufgetreten ist

Nachdem Sie den Generierungsbezeichner des virtuellen Computers abgerufen haben, sollten Sie ihn zur zukünftigen Verwendung speichern. Bevor Ihre App einen zeitkritischen Vorgang ausführt, z. B. das Committen in eine Datenbank, sollten Sie den Generierungsbezeichner erneut abrufen und mit dem gespeicherten Wert vergleichen. Wenn sich der Bezeichner geändert hat, bedeutet dies, dass ein Zeitverschiebungsereignis aufgetreten ist und Ihre App entsprechend agieren muss.

 

 
