---
title: Erkennen des Setupstatus
description: Erkennen des Setupstatus
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Medienformat-SDK, Softwareverteilung
- Advanced Systems Format (ASF), Softwareverteilung
- ASF (Advanced Systems Format), Softwareverteilung
- Windows Media Format SDK,redistribution
- Advanced Systems Format (ASF), Redistribution
- ASF (Advanced Systems Format), Redistribution
- Softwareverteilung, Erkennen des Setupstatus
- Redistribution,Detecting setup status (Neuverteilung,Erkennen des Setupstatus)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250ab87fd81592b868e1dbf13106577f83e680796310aff246f0c1483fa847cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931391"
---
# <a name="detecting-setup-status"></a>Erkennen des Setupstatus

Wenn die ausführbare Datei für die Weiterverteilung auf einem Computer ausgeführt wird, wird der Installationsstatus in der Registrierung als **HRESULT-Wert** erfasst. Der Installationsstatus wird im Registrierungseintrag **InstallResult** unter dem folgenden Unterschlüssel gespeichert:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Setup**

Der **Registrierungseintrag InstallResult** hat das folgende Formular.



| Name              | type           | Wert                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Ein **HRESULT,** das angibt, Windows Media Player erfolgreich installiert wurde und ob ein Neustart erforderlich ist. |



 

Mit dem folgenden Code werden die *Variablen fSucess* und *fRebootNeeded* auf **True** oder **False** festgelegt. Dies basiert auf dem **HRESULT-Wert,** der vom Windows Media Setup im Komponentenverteilungspaket geschrieben wurde.


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

[**Software Redistribution**](software-redistribution.md)
</dt> </dl>

 

 




