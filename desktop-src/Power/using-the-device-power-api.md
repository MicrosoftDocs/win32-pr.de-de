---
description: Verwenden Sie die Programmierelemente Device Power, um die Leistung von Geräten zu verwalten, während sich das System im Ruhezustand befindet.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Verwenden der Geräte-Power-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aff8239c1cd0ffc8d5e8abaf0133a9ca42bb3a01a5b6fc2acef7850929a8484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032770"
---
# <a name="using-the-device-power-api"></a>Verwenden der Geräte-Power-API

Verwenden Sie die Programmierelemente Device Power, um die Leistung von Geräten zu verwalten, während sich das System im Ruhezustand befindet.

## <a name="opening-and-closing-the-device-list"></a>Öffnen und Schließen der Geräteliste

Das Öffnen und Schließen der Geräteliste ist ein kostspieliger Prozess in Bezug auf die CPU-Zeit. Die [**Funktionen DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) und [**DevicePowerClose,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) die dies tun, sind nur erforderlich, wenn die Anwendung die Geräteliste mehrmals abfragen muss.

Wenn [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) aufgerufen wird, [**muss DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) aufgerufen werden, wenn Gerätelistenabfragen abgeschlossen sind. [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) und [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) schließen die Geräteliste nicht, wenn sie explizit von **DevicePowerOpen geöffnet wurde.**

## <a name="enumerating-devices"></a>Enumerieren von Geräten

Die [**DevicePowerEnumDevices-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) erkennt, ob die Geräteliste geöffnet ist, und öffnet sie, falls nicht, sie. **DevicePowerEnumDevices** zählt die Geräte basierend auf den angegebenen Suchkriterien auf. Wenn die Geräteliste von der Funktion geöffnet wurde, wird sie geschlossen, bevor die Funktion zurückgegeben wird.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Aktivieren und Deaktivieren eines Geräts, um das System zu aktivieren und zu deaktivieren

Die [**DevicePowerSetDeviceState-Funktion,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) ähnlich [**wie DevicePowerEnumDevices,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)erkennt, ob die Geräteliste geöffnet ist, und öffnet sie, falls nicht, sie. **DevicePowerSetDeviceState** legt dann die angegebenen Kriterien für das angegebene Gerät fest. Wenn die Geräteliste von der Funktion geöffnet wurde, wird sie geschlossen, bevor die Funktion zurückgegeben wird.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird die Verwendung der Geräte-Power-API veranschaulicht.


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



In diesem Beispiel wird die Geräteliste einmal geöffnet und einmal geschlossen. Wenn [**die Funktionen DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) und [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) nicht aufgerufen würden, wäre die Geräteliste durch jeden Aufruf von [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) und [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)geöffnet und geschlossen worden. Mit **DevicePowerOpen und** **DevicePowerClose** haben wir das Öffnen der Geräteliste zweimal unnötig gespeichert.

 

 



