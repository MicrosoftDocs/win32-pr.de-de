---
title: Erkennen des Setupstatus für Windows Medieneinrichtung
description: Erkennen des Setupstatus für Windows Medieneinrichtung
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player,Erkennen des Setupstatus
- Windows Media Player,Setupstatus
- Windows Media Player,Verteilen von Software
- Windows Media Player,Softwareverteilung
- Erkennen des Setupstatus
- Setupstatus
- Verteilen von Software
- Softwareverteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797c7cb5fe4d34895109777c4da7e15489a0d32acd9cf42660b3346521f6f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340899"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Erkennen des Setupstatus für Windows Medieneinrichtung

Der folgende Code kann mit der -Windows Media Player-Paketen verwendet werden. Der Installationsstatus wird im Registrierungseintrag **InstallResult** unter dem folgenden Unterschlüssel gespeichert:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Setup**

Der **Registrierungseintrag InstallResult** hat das folgende Formular.



| Name              | Typ           | Wert                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | Ein **HRESULT,** das angibt, Windows Media Player erfolgreich installiert wurde und ob ein Neustart erforderlich ist. |



 

Hier ist ein C++-Beispielcode, der in eine aufrufende Setupanwendung integriert werden kann. Dieser Code setzt die Variablen und je nach Fall auf true oder false, basierend auf dem `fSuccess` `fRebootNeeded`   **HRESULT-Wert,** der von Windows Media Player Setup im Komponentenverteilungspaket geschrieben wurde.


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
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verteilen Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




