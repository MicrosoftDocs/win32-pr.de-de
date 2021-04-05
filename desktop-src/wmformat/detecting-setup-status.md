---
title: Ermitteln des Setup Status
description: Ermitteln des Setup Status
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media-Format-SDK, Software Verteilung
- Advanced Systems Format (ASF), Software Verteilung
- ASF (Advanced Systems Format), Software Verteilung
- SDK für Windows Media-Format, Neuverteilung
- Advanced Systems Format (ASF), Verteilung
- ASF (Advanced Systems Format), Verteilung
- Software Verteilung, Ermitteln des Setup Status
- Verteilung, Ermitteln des Setup Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714219"
---
# <a name="detecting-setup-status"></a>Ermitteln des Setup Status

Wenn die ausführbare Datei für die erneute Verteilung auf einem Computer ausgeführt wird, wird der Installationsstatus in der Registrierung als **HRESULT** -Wert aufgezeichnet. Der Installationsstatus wird im Registrierungs Eintrag **installresult** unter dem folgenden Unterschlüssel gespeichert:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player- \\ Setup**

Der Registrierungs Eintrag **installresult** weist das folgende Format auf:



| Name              | type           | Wert                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **Installresult** | **REG \_ DWORD** | Ein **HRESULT** , das angibt, ob die Windows Media Player-Installation erfolgreich war und ob ein Neustart erforderlich ist. |



 

Der folgende Code legt die Variablen *fsucess* und *frebootbenöggf* **. auf Grundlage** des **HRESULT** -Werts **fest, der** von der Windows Media-Installation im Komponenten Weitergabepaket geschrieben wird.


```C++
#include <windows.h>
#include <stdio.h>

// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
  
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Software Verteilung**](software-redistribution.md)
</dt> </dl>

 

 




