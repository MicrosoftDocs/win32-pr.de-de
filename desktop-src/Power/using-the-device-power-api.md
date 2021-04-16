---
description: Verwenden Sie die Elemente der Geräte Energie Programmierung, um die Art der Ausführung von Geräten zu verwalten, während sich das System im Ruhezustand befindet.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Verwenden der Device Power-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529099"
---
# <a name="using-the-device-power-api"></a><span data-ttu-id="9fa31-103">Verwenden der Device Power-API</span><span class="sxs-lookup"><span data-stu-id="9fa31-103">Using the Device Power API</span></span>

<span data-ttu-id="9fa31-104">Verwenden Sie die Elemente der Geräte Energie Programmierung, um die Art der Ausführung von Geräten zu verwalten, während sich das System im Ruhezustand befindet.</span><span class="sxs-lookup"><span data-stu-id="9fa31-104">Use the Device Power programming elements to manage the way devices perform while the system is in a sleep state.</span></span>

## <a name="opening-and-closing-the-device-list"></a><span data-ttu-id="9fa31-105">Öffnen und Schließen der Geräteliste</span><span class="sxs-lookup"><span data-stu-id="9fa31-105">Opening and closing the device list</span></span>

<span data-ttu-id="9fa31-106">Das Öffnen und Schließen der Geräteliste ist ein kostspieliger Prozess in Bezug auf die CPU-Zeit.</span><span class="sxs-lookup"><span data-stu-id="9fa31-106">Opening and closing the device list is a costly process in terms of CPU time.</span></span> <span data-ttu-id="9fa31-107">Die Funktionen [**devicepoweropen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) und [**devicepowerclose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) sind nur erforderlich, wenn die Anwendung die Geräteliste mehrmals Abfragen muss.</span><span class="sxs-lookup"><span data-stu-id="9fa31-107">The [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions that do this are only necessary if the application needs to query the device list multiple times.</span></span>

<span data-ttu-id="9fa31-108">Wenn [**devicepoweropen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) aufgerufen wird, muss [**devicepowerclose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) aufgerufen werden, wenn Gerätelisten Abfragen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="9fa31-108">If [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) is called, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) must be called when device-list queries are complete.</span></span> <span data-ttu-id="9fa31-109">[**Devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) und [**devicepowersettovicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) schließen die Geräteliste nicht, wenn Sie explizit von **devicepoweropen** geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="9fa31-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) will not close the device list if it has been explicitly opened by **DevicePowerOpen**.</span></span>

## <a name="enumerating-devices"></a><span data-ttu-id="9fa31-110">Enumerieren von Geräten</span><span class="sxs-lookup"><span data-stu-id="9fa31-110">Enumerating devices</span></span>

<span data-ttu-id="9fa31-111">Die [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) -Funktion erkennt, ob die Geräteliste geöffnet ist, und öffnet Sie, falls nicht, Sie.</span><span class="sxs-lookup"><span data-stu-id="9fa31-111">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="9fa31-112">**Devicepowerenumdevices** listet die Geräte auf der Grundlage der angegebenen Suchkriterien auf.</span><span class="sxs-lookup"><span data-stu-id="9fa31-112">**DevicePowerEnumDevices** enumerates the devices based on the specified search criteria.</span></span> <span data-ttu-id="9fa31-113">Wenn die Geräteliste von der Funktion geöffnet wurde, wird Sie geschlossen, bevor die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9fa31-113">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a><span data-ttu-id="9fa31-114">Aktivieren und Deaktivieren eines Geräts vor dem Reaktivieren des Systems</span><span class="sxs-lookup"><span data-stu-id="9fa31-114">Enabling and disabling a device from waking the system</span></span>

<span data-ttu-id="9fa31-115">Die [**devicepowersettovicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) -Funktion, ähnlich wie [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), erkennt, ob die Geräteliste geöffnet ist, und öffnet Sie, falls nicht, Sie.</span><span class="sxs-lookup"><span data-stu-id="9fa31-115">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function, similar to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="9fa31-116">**Devicepowersetabvicestate** legt die angegebenen Kriterien für das angegebene Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="9fa31-116">**DevicePowerSetDeviceState** then sets the specified criteria for the specified device.</span></span> <span data-ttu-id="9fa31-117">Wenn die Geräteliste von der Funktion geöffnet wurde, wird Sie geschlossen, bevor die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9fa31-117">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="example-code"></a><span data-ttu-id="9fa31-118">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="9fa31-118">Example Code</span></span>

<span data-ttu-id="9fa31-119">Im folgenden Beispiel wird die Verwendung der Device Power API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9fa31-119">The following example demonstrates the use of the Device Power API.</span></span>


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



<span data-ttu-id="9fa31-120">In diesem Beispiel wird die Geräteliste einmal geöffnet und einmal geschlossen.</span><span class="sxs-lookup"><span data-stu-id="9fa31-120">In this example the device list is opened once, and closed once.</span></span> <span data-ttu-id="9fa31-121">Wenn die Funktionen [**devicepoweropen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) und [**devicepowerclose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) nicht aufgerufen wurden, wurde die Geräteliste durch jeden Aufruf von [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) und [**devicepowersetdevicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)geöffnet und geschlossen.</span><span class="sxs-lookup"><span data-stu-id="9fa31-121">If the [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions were not called, the device list would have been opened and closed by each call to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span></span> <span data-ttu-id="9fa31-122">Mithilfe von **devicepoweropen** und **devicepowerclose** haben wir zwei unnötige Zeit zum Öffnen der Geräteliste gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9fa31-122">By using **DevicePowerOpen** and **DevicePowerClose** we saved opening the device list two unnecessary times.</span></span>

 

 



