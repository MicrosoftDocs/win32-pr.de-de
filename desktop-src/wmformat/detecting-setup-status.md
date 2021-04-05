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
# <a name="detecting-setup-status"></a><span data-ttu-id="7cab0-111">Ermitteln des Setup Status</span><span class="sxs-lookup"><span data-stu-id="7cab0-111">Detecting Setup Status</span></span>

<span data-ttu-id="7cab0-112">Wenn die ausführbare Datei für die erneute Verteilung auf einem Computer ausgeführt wird, wird der Installationsstatus in der Registrierung als **HRESULT** -Wert aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cab0-112">When the redistribution executable runs on a computer, it records its installation status in the registry as an **HRESULT** value.</span></span> <span data-ttu-id="7cab0-113">Der Installationsstatus wird im Registrierungs Eintrag **installresult** unter dem folgenden Unterschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="7cab0-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="7cab0-114">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player- \\ Setup**</span><span class="sxs-lookup"><span data-stu-id="7cab0-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="7cab0-115">Der Registrierungs Eintrag **installresult** weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="7cab0-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="7cab0-116">Name</span><span class="sxs-lookup"><span data-stu-id="7cab0-116">Name</span></span>              | <span data-ttu-id="7cab0-117">type</span><span class="sxs-lookup"><span data-stu-id="7cab0-117">Type</span></span>           | <span data-ttu-id="7cab0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7cab0-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cab0-119">**Installresult**</span><span class="sxs-lookup"><span data-stu-id="7cab0-119">**InstallResult**</span></span> | <span data-ttu-id="7cab0-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7cab0-120">**REG\_DWORD**</span></span> | <span data-ttu-id="7cab0-121">Ein **HRESULT** , das angibt, ob die Windows Media Player-Installation erfolgreich war und ob ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7cab0-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="7cab0-122">Der folgende Code legt die Variablen *fsucess* und *frebootbenöggf* **. auf Grundlage** des **HRESULT** -Werts **fest, der** von der Windows Media-Installation im Komponenten Weitergabepaket geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7cab0-122">The following code will set the *fSucess* and *fRebootNeeded* variables to **True** or **False**, as appropriate, based on the **HRESULT** value written by Windows Media setup in the component redistribution package.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7cab0-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cab0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cab0-124">**Software Verteilung**</span><span class="sxs-lookup"><span data-stu-id="7cab0-124">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




