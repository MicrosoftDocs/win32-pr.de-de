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
# <a name="using-the-device-power-api"></a>Verwenden der Device Power-API

Verwenden Sie die Elemente der Geräte Energie Programmierung, um die Art der Ausführung von Geräten zu verwalten, während sich das System im Ruhezustand befindet.

## <a name="opening-and-closing-the-device-list"></a>Öffnen und Schließen der Geräteliste

Das Öffnen und Schließen der Geräteliste ist ein kostspieliger Prozess in Bezug auf die CPU-Zeit. Die Funktionen [**devicepoweropen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) und [**devicepowerclose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) sind nur erforderlich, wenn die Anwendung die Geräteliste mehrmals Abfragen muss.

Wenn [**devicepoweropen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) aufgerufen wird, muss [**devicepowerclose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) aufgerufen werden, wenn Gerätelisten Abfragen abgeschlossen sind. [**Devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) und [**devicepowersettovicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) schließen die Geräteliste nicht, wenn Sie explizit von **devicepoweropen** geöffnet wurde.

## <a name="enumerating-devices"></a>Enumerieren von Geräten

Die [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) -Funktion erkennt, ob die Geräteliste geöffnet ist, und öffnet Sie, falls nicht, Sie. **Devicepowerenumdevices** listet die Geräte auf der Grundlage der angegebenen Suchkriterien auf. Wenn die Geräteliste von der Funktion geöffnet wurde, wird Sie geschlossen, bevor die Funktion zurückgegeben wird.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Aktivieren und Deaktivieren eines Geräts vor dem Reaktivieren des Systems

Die [**devicepowersettovicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) -Funktion, ähnlich wie [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), erkennt, ob die Geräteliste geöffnet ist, und öffnet Sie, falls nicht, Sie. **Devicepowersetabvicestate** legt die angegebenen Kriterien für das angegebene Gerät fest. Wenn die Geräteliste von der Funktion geöffnet wurde, wird Sie geschlossen, bevor die Funktion zurückgegeben wird.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird die Verwendung der Device Power API veranschaulicht.


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



In diesem Beispiel wird die Geräteliste einmal geöffnet und einmal geschlossen. Wenn die Funktionen [**devicepoweropen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) und [**devicepowerclose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) nicht aufgerufen wurden, wurde die Geräteliste durch jeden Aufruf von [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) und [**devicepowersetdevicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)geöffnet und geschlossen. Mithilfe von **devicepoweropen** und **devicepowerclose** haben wir zwei unnötige Zeit zum Öffnen der Geräteliste gespeichert.

 

 



