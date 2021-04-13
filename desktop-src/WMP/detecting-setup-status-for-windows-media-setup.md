---
title: Ermitteln des Setup Status für die Windows Media-Installation
description: Ermitteln des Setup Status für die Windows Media-Installation
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player, Ermitteln des Setup Status
- Windows Media Player, Setup Status
- Windows Media Player, Neuverteilen von Software
- Windows Media Player, Software Verteilung
- Ermitteln des Setup Status
- Setup Status
- Neuverteilen von Software
- Software Verteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388677"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Ermitteln des Setup Status für die Windows Media-Installation

Der folgende Code kann mit den Windows-Media Player-weitergabepaketen verwendet werden. Der Installationsstatus wird im Registrierungs Eintrag **installresult** unter dem folgenden Unterschlüssel gespeichert:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player- \\ Setup**

Der Registrierungs Eintrag **installresult** weist das folgende Format auf:



| Name              | type           | Wert                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **Installresult** | **REG \_ DWORD** | Ein **HRESULT** , das angibt, ob die Windows Media Player-Installation erfolgreich war und ob ein Neustart erforderlich ist. |



 

Im folgenden finden Sie ein Beispiel für C++-Code, der in eine aufrufende Setup Anwendung integriert werden kann. Mit diesem Code werden die `fSuccess` `fRebootNeeded` Variablen und entsprechend dem **HRESULT** -Wert, der von der Windows Media Player-Einrichtung im Komponenten Weitergabepaket geschrieben wurde, auf **true** oder **false** festgelegt.


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

[**Neuverteilen von Windows Media Player-Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




