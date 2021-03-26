---
description: Im folgenden Codebeispiel wird gezeigt, wie mit EnumDisplayDevices Informationen zu einem Bildschirm angezeigt werden.
ms.assetid: 8c2420de-292f-481e-b06b-54cc174a8faf
title: Informationen zu einem Anzeige Monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8b120563e9ceed2e87d66e5bb79790a0f7c771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993990"
---
# <a name="getting-information-on-a-display-monitor"></a><span data-ttu-id="4953e-103">Informationen zu einem Anzeige Monitor</span><span class="sxs-lookup"><span data-stu-id="4953e-103">Getting Information on a Display Monitor</span></span>

<span data-ttu-id="4953e-104">Im folgenden Codebeispiel wird gezeigt, wie mit [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) Informationen zu einem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4953e-104">The following code sample shows how to use [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) to get information on a display monitor.</span></span>


```C++
BOOL GetDisplayMonitorInfo(int nDeviceIndex, LPSTR lpszMonitorInfo)
{
    FARPROC EnumDisplayDevices;
    HINSTANCE  hInstUser32;
    DISPLAY_DEVICE DispDev; 
    char szSaveDeviceName[33];  // 32 + 1 for the null-terminator 
    BOOL bRet = TRUE;
        HRESULT hr;
    
    hInstUser32 = LoadLibrary("c:\\windows\User32.DLL");
    if (!hInstUser32) return FALSE;  
    
    // Get the address of the EnumDisplayDevices function 
    EnumDisplayDevices = (FARPROC)GetProcAddress(hInstUser32,"EnumDisplayDevicesA");
    if (!EnumDisplayDevices) {
        FreeLibrary(hInstUser32);
        return FALSE;
    }

    ZeroMemory(&DispDev, sizeof(DispDev));
    DispDev.cb = sizeof(DispDev); 
    
    // After the first call to EnumDisplayDevices,  
    // DispDev.DeviceString is the adapter name 
    if (EnumDisplayDevices(NULL, nDeviceIndex, &DispDev, 0)) 
        {  
                hr = StringCchCopy(szSaveDeviceName, 33, DispDev.DeviceName);
                if (FAILED(hr))
                {
                // TODO: write error handler 
                }
        
        // After second call, DispDev.DeviceString is the  
        // monitor name for that device  
        EnumDisplayDevices(szSaveDeviceName, 0, &DispDev, 0);   
        
                // In the following, lpszMonitorInfo must be 128 + 1 for  
                // the null-terminator. 
                hr = StringCchCopy(lpszMonitorInfo, 129, DispDev.DeviceString);
                if (FAILED(hr))
                {
                // TODO: write error handler 
                }
                
    } else    {
        bRet = FALSE;
    }

    FreeLibrary(hInstUser32);

    return bRet;
}
```



 

 



