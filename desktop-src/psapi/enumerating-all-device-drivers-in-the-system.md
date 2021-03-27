---
title: Auflisten aller Gerätetreiber im System
description: Der folgende Beispielcode verwendet die enumdevicedrivers-Funktion, um die aktuellen Gerätetreiber im System aufzulisten.
ms.assetid: 047d8541-e17e-4738-8453-674db69365df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b02345f5d59979fe3576fd952c056ca808e6ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947524"
---
# <a name="enumerating-all-device-drivers-in-the-system"></a>Auflisten aller Gerätetreiber im System

Der folgende Beispielcode verwendet die [**enumdevicedrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) -Funktion, um die aktuellen Gerätetreiber im System aufzulisten. Sie übergibt die Lade Adressen, die von diesem Funktions aufgerufenen abgerufen wurden, an die [**getdevicedriverbasename**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) -Funktion, um einen Namen abzurufen, der angezeigt werden kann.


```C++
#include <windows.h>
#include <psapi.h>
#include <tchar.h>
#include <stdio.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

#define ARRAY_SIZE 1024

int main( void )
{
   LPVOID drivers[ARRAY_SIZE];
   DWORD cbNeeded;
   int cDrivers, i;

   if( EnumDeviceDrivers(drivers, sizeof(drivers), &cbNeeded) && cbNeeded < sizeof(drivers))
   { 
      TCHAR szDriver[ARRAY_SIZE];

      cDrivers = cbNeeded / sizeof(drivers[0]);

      _tprintf(TEXT("There are %d drivers:\n"), cDrivers);      
      for (i=0; i < cDrivers; i++ )
      {
         if(GetDeviceDriverBaseName(drivers[i], szDriver, sizeof(szDriver) /              sizeof(szDriver[0])))
         {
            _tprintf(TEXT("%d: %s\n"), i+1, szDriver);
         }
      }
   }
   else 
   {
        _tprintf(TEXT("EnumDeviceDrivers failed; array size needed is %d\n"),             cbNeeded / sizeof(LPVOID));
        return 1;
   }

return 0;
}
```



 

 




