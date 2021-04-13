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
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="a6da2-111">Ermitteln des Setup Status für die Windows Media-Installation</span><span class="sxs-lookup"><span data-stu-id="a6da2-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="a6da2-112">Der folgende Code kann mit den Windows-Media Player-weitergabepaketen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6da2-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="a6da2-113">Der Installationsstatus wird im Registrierungs Eintrag **installresult** unter dem folgenden Unterschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="a6da2-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="a6da2-114">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player- \\ Setup**</span><span class="sxs-lookup"><span data-stu-id="a6da2-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="a6da2-115">Der Registrierungs Eintrag **installresult** weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="a6da2-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="a6da2-116">Name</span><span class="sxs-lookup"><span data-stu-id="a6da2-116">Name</span></span>              | <span data-ttu-id="a6da2-117">type</span><span class="sxs-lookup"><span data-stu-id="a6da2-117">Type</span></span>           | <span data-ttu-id="a6da2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a6da2-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6da2-119">**Installresult**</span><span class="sxs-lookup"><span data-stu-id="a6da2-119">**InstallResult**</span></span> | <span data-ttu-id="a6da2-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6da2-120">**REG\_DWORD**</span></span> | <span data-ttu-id="a6da2-121">Ein **HRESULT** , das angibt, ob die Windows Media Player-Installation erfolgreich war und ob ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a6da2-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="a6da2-122">Im folgenden finden Sie ein Beispiel für C++-Code, der in eine aufrufende Setup Anwendung integriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6da2-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="a6da2-123">Mit diesem Code werden die `fSuccess` `fRebootNeeded` Variablen und entsprechend dem **HRESULT** -Wert, der von der Windows Media Player-Einrichtung im Komponenten Weitergabepaket geschrieben wurde, auf **true** oder **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6da2-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a6da2-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6da2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6da2-125">**Neuverteilen von Windows Media Player-Software**</span><span class="sxs-lookup"><span data-stu-id="a6da2-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




