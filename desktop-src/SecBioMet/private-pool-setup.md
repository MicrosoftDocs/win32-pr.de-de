---
title: Einrichtung des privaten Pools
description: Enthält das Setup Konsolen Projekt.
ms.assetid: 0B00690C-9B13-4D8B-8AB6-F8BD2E35858C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a661e65610e6cefb03ee9d47f70d7dc8d6d92a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037392"
---
# <a name="private-pool-setup"></a><span data-ttu-id="b3ab1-103">Einrichtung des privaten Pools</span><span class="sxs-lookup"><span data-stu-id="b3ab1-103">Private Pool Setup</span></span>

<span data-ttu-id="b3ab1-104">Die folgenden Abschnitte enthalten den Code, der zum Einrichten eines privaten Sensor Pools erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-104">The following sections contain the code necessary to setup a private sensor pool.</span></span>

-   [<span data-ttu-id="b3ab1-105">Targetver. h</span><span class="sxs-lookup"><span data-stu-id="b3ab1-105">Targetver.h</span></span>](#targetverh)
-   [<span data-ttu-id="b3ab1-106">stdafx.h</span><span class="sxs-lookup"><span data-stu-id="b3ab1-106">Stdafx.h</span></span>](#stdafxh)
-   [<span data-ttu-id="b3ab1-107">Privatepoolcommondefs. h</span><span class="sxs-lookup"><span data-stu-id="b3ab1-107">PrivatePoolCommonDefs.h</span></span>](#privatepoolcommondefsh)
-   [<span data-ttu-id="b3ab1-108">Privatepoolsetup. cpp</span><span class="sxs-lookup"><span data-stu-id="b3ab1-108">PrivatePoolSetup.cpp</span></span>](#privatepoolsetupcpp)

## <a name="targetverh"></a><span data-ttu-id="b3ab1-109">Targetver. h</span><span class="sxs-lookup"><span data-stu-id="b3ab1-109">Targetver.h</span></span>

<span data-ttu-id="b3ab1-110">Dieses Beispiel wurde für Windows 7 und spätere Betriebssysteme erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-110">This sample was created for Windows 7 and later operating systems.</span></span>


```C++
#pragma once
#ifndef _WIN32_WINNT            
#define _WIN32_WINNT NTDDI_WIN7 
#endif
```



## <a name="stdafxh"></a><span data-ttu-id="b3ab1-111">stdafx.h</span><span class="sxs-lookup"><span data-stu-id="b3ab1-111">Stdafx.h</span></span>


```C++
// stdafx.h : include file for standard system include files,
// or project specific include files that are used frequently but
// are changed infrequently
//
#pragma once

#include "targetver.h"

// Use secure (template) versions of nonsecure 
// CRT text routines
#define _CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES     1

#include <stdio.h>
#include <tchar.h>

#include <windows.h>
#include <winbio.h>

#include "BioHelper.h"

#ifndef ARGUMENT_PRESENT
#define ARGUMENT_PRESENT(x) (((x) != NULL))
#endif
```



## <a name="privatepoolcommondefsh"></a><span data-ttu-id="b3ab1-112">Privatepoolcommondefs. h</span><span class="sxs-lookup"><span data-stu-id="b3ab1-112">PrivatePoolCommonDefs.h</span></span>

<span data-ttu-id="b3ab1-113">Fügen Sie den folgenden Header ein.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-113">Include the following header.</span></span> <span data-ttu-id="b3ab1-114">Beachten Sie, dass Sie eine eindeutige Datenbank-ID generieren müssen.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-114">Note that you must generate a unique database ID.</span></span> <span data-ttu-id="b3ab1-115">Verwenden Sie die bereitgestellte GUID nicht in einer freigegebenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-115">Do not use the provided GUID in a released application.</span></span>


```C++
/******************************************************************************
THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED
TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.

This source code is only intended as a supplement to Microsoft Development
Tools and/or WinHelp documentation.  See these sources for detailed information
regarding the Microsoft samples programs.
******************************************************************************/

#pragma once

// Common defintions used by all three programs

// NOTE: DO *NOT* USE THIS GUID VALUE FOR A REAL
// APPLICATION. GENERATE YOUR OWN UNIQUE GUID AND
// REPLACE THE FOLLOWING DEFINITION!
//
// {5086745D-B3F9-4da7-859E-9CC4331CE47C}
static const GUID PRIVATE_POOL_DATABASE_ID = 
{ 0x5086745d, 0xb3f9, 0x4da7, { 0x85, 0x9e, 0x9c, 0xc4, 0x33, 0x1c, 0xe4, 0x7c } };
```



## <a name="privatepoolsetupcpp"></a><span data-ttu-id="b3ab1-116">Privatepoolsetup. cpp</span><span class="sxs-lookup"><span data-stu-id="b3ab1-116">PrivatePoolSetup.cpp</span></span>

<span data-ttu-id="b3ab1-117">Der folgende Quellcode zeigt den Einstiegspunkt für eine private Sensor Pool Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b3ab1-117">The following source code displays the entry point for a private sensor pool application.</span></span>


```C++
/******************************************************************************
THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED
TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.

This source code is only intended as a supplement to Microsoft Development
Tools and/or WinHelp documentation.  See these sources for detailed information
regarding the Microsoft samples programs.
******************************************************************************/

// PrivatePoolSetup.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"
#include "PrivatePoolCommonDefs.h"   // From Private Pool Setup
#include "Strsafe.h"                 // For StringCbGets()

#include <vector>

// Forward declarations of local functions.
//
static void onInstall();
static void onUninstall();
static void onAdd();
static void onRemove();

static bool selectSensorMenu(
    __in LPCTSTR Prompt,
    __in WINBIO_UNIT_SCHEMA *UnitArray,
    __in SIZE_T UnitCount,
    __out SIZE_T *SelectedUnit
    );

static bool isDatabaseInstalled(
    __in WINBIO_UUID *DatabaseId,
    __out WINBIO_UUID *DataFormat
    );

//-----------------------------------------------------------------------------

int _tmain(int argc, _TCHAR* argv[])
{
    HRESULT hr = S_OK;
    bool databaseInstalled = false;
    WINBIO_UUID dataFormat = {};

    _tprintf( _T("\nWinBio Private Pool Setup\n\n"));

    if (argc < 2)
    {
        _tprintf(_T("Usage: %s -install | -uninstall | -add | -remove\n"), argv[0]);
        _tprintf(
            _T("\n")
            _T("  -install      define private template database\n")
            _T("  -uninstall    detach all sensors from private database and delete database\n")
            _T("  -add          attach (one) specific sensor to private database\n")
            _T("  -remove       detach (one) specific sensor from private database\n")
            _T("\n")
            );
    }
    else
    {
        if (_tcsicmp( argv[1], _T("-install")) == 0)
        {
            onInstall();
        }
        else if (_tcsicmp( argv[1], _T("-uninstall")) == 0)
        {
            onUninstall();
        }
        else if (_tcsicmp( argv[1], _T("-add")) == 0)
        {
            onAdd();
        }
        else if (_tcsicmp( argv[1], _T("-remove")) == 0)
        {
            onRemove();
        }
        else
        {
            _tprintf(_T("*** Error - Unknown command option: %s\n"), argv[1]);
        }
    }

    return 0;
}

//-----------------------------------------------------------------------------

static void onInstall()
{
    WINBIO_UUID databaseId = PRIVATE_POOL_DATABASE_ID;
    WINBIO_UUID dataFormat = {};

    if (isDatabaseInstalled( &databaseId, &dataFormat))
    {
        _tprintf(_T("*** Error - private database already installed.\n"));
        return;
    }

    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;
    HRESULT hr = WinBioEnumBiometricUnits( 
                    WINBIO_TYPE_FINGERPRINT, 
                    &unitArray, 
                    &unitCount 
                    );
    if (SUCCEEDED(hr))
    {
        SIZE_T selectedUnit = 0;
        if (selectSensorMenu( 
                _T("Make templates compatible with the selected sensor"), 
                unitArray, 
                unitCount, 
                &selectedUnit
                ))
        {
            BioHelper::POOL_CONFIGURATION derivedConfig = {};
            hr = BioHelper::CreateCompatibleConfiguration( 
                    &unitArray[selectedUnit], 
                    &derivedConfig 
                    );
            if (SUCCEEDED(hr))
            {
                WINBIO_STORAGE_SCHEMA storageSchema = {};
                storageSchema.DatabaseId = PRIVATE_POOL_DATABASE_ID;
                storageSchema.DataFormat = derivedConfig.DataFormat;
                storageSchema.Attributes = derivedConfig.DatabaseAttributes;
                hr = BioHelper::RegisterDatabase( &storageSchema );
            }
        }
        else
        {
            hr = E_INVALIDARG;
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }
    if (SUCCEEDED(hr))
    {
        _tprintf(_T("- Private database installed.\n"));
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static void onUninstall()
{
    WINBIO_UUID databaseId = PRIVATE_POOL_DATABASE_ID;
    WINBIO_UUID dataFormat = {};

    if (!isDatabaseInstalled( &databaseId, &dataFormat))
    {
        _tprintf(_T("*** Error - private database not installed.\n"));
        return;
    }

    // Remove biometric unit registrations.
    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;

    HRESULT hr = WinBioEnumBiometricUnits( 
                    WINBIO_TYPE_FINGERPRINT, 
                    &unitArray, 
                    &unitCount 
                    );
    if (SUCCEEDED(hr))
    {
        for (SIZE_T i = 0; i < unitCount; ++i)
        {
            bool configRemoved = false;
            hr = BioHelper::UnregisterPrivateConfiguration( 
                                &unitArray[i], 
                                &databaseId, 
                                &configRemoved 
                                );
            if (FAILED(hr))
            {
                break;
            }
            if (configRemoved)
            {
                _tprintf(
                    _T("- Sensor removed from private pool: %ls (%ls)\n"), 
                    unitArray[i].Manufacturer, 
                    unitArray[i].Description 
                    );
            }
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }

    if (SUCCEEDED(hr))
    {
        // Remove the database.
        hr = BioHelper::UnregisterDatabase( &databaseId );
    }
    if (SUCCEEDED(hr))
    {
        _tprintf(_T("- Private database uninstalled.\n"));
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static void onAdd()
{
    WINBIO_UUID databaseId = PRIVATE_POOL_DATABASE_ID;
    WINBIO_UUID dataFormat = {};

    if (!isDatabaseInstalled( &databaseId, &dataFormat))
    {
        _tprintf(_T("*** Error - private database not installed.\n"));
        return;
    }

    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;
    HRESULT hr = WinBioEnumBiometricUnits( 
                    WINBIO_TYPE_FINGERPRINT, 
                    &unitArray, 
                    &unitCount 
                    );
    if (SUCCEEDED(hr))
    {
        SIZE_T selectedUnit = 0;
        if (selectSensorMenu( 
                _T("Choose a sensor to add to the private pool"), 
                unitArray, 
                unitCount, 
                &selectedUnit
                ))
        {
            BioHelper::POOL_CONFIGURATION derivedConfig = {};
            hr = BioHelper::CreateCompatibleConfiguration( 
                    &unitArray[selectedUnit], 
                    &derivedConfig 
                    );
            if (SUCCEEDED(hr))
            {
                derivedConfig.DatabaseId = PRIVATE_POOL_DATABASE_ID;
                hr = BioHelper::RegisterPrivateConfiguration( 
                                    &unitArray[selectedUnit], 
                                    &derivedConfig 
                                    );
            }
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }
    if (SUCCEEDED(hr))
    {
        _tprintf(_T("- Sensor added to private pool.\n"));
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static void onRemove()
{
    bool configRemoved = false;
    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;
    HRESULT hr = WinBioEnumBiometricUnits( 
            WINBIO_TYPE_FINGERPRINT, 
            &unitArray, 
            &unitCount 
            );
    if (SUCCEEDED(hr))
    {
        SIZE_T selectedUnit = 0;
        if (selectSensorMenu( 
                _T("Choose a sensor to remove from the private pool"), 
                unitArray, 
                unitCount, 
                &selectedUnit
                ))
        {
            WINBIO_UUID targetDatabase = PRIVATE_POOL_DATABASE_ID;
            hr = BioHelper::UnregisterPrivateConfiguration( 
                                &unitArray[selectedUnit], 
                                &targetDatabase,
                                &configRemoved
                                );
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }
    if (SUCCEEDED(hr))
    {
        if (configRemoved)
        {
            _tprintf(_T("- Sensor removed from private pool.\n"));
        }
        else
        {
            _tprintf(_T("*** Error - selected sensor not a member of private pool.\n"));
        }
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static bool selectSensorMenu(
    __in LPCTSTR Prompt,
    __in WINBIO_UNIT_SCHEMA *UnitArray,
    __in SIZE_T UnitCount,
    __out SIZE_T *SelectedUnit
    )
{
    if (!ARGUMENT_PRESENT(UnitArray) ||
        !ARGUMENT_PRESENT(SelectedUnit) ||
        UnitCount == 0)
    {
        return false;
    }

    _tprintf(_T("\n%s:\n\n"), Prompt);
    for (SIZE_T i = 0; i < UnitCount; ++i)
    {
        _tprintf(
            _T(" %3d - %ls (%ls)\n"), 
            (i + 1), 
            UnitArray[i].Manufacturer, 
            UnitArray[i].Description 
            );
    }

    _tprintf(_T("\nSelect sensor and press <ENTER>: "));
    TCHAR buffer[20] = {};
    HRESULT hr = StringCbGets( buffer, 20*sizeof(TCHAR) );
    _tprintf(_T("\n"));

    int selected = _tstoi( buffer );
    if (selected <= 0 ||
        selected > (int)UnitCount)
    {
        return false;
    }
    *SelectedUnit = (SIZE_T)(selected - 1);
    return true;
}

//-----------------------------------------------------------------------------

static bool isDatabaseInstalled(
    __in WINBIO_UUID *DatabaseId,
    __out WINBIO_UUID *DataFormat
    )
{
    if (!ARGUMENT_PRESENT(DatabaseId) ||
        !ARGUMENT_PRESENT(DataFormat))
    {
        return false;
    }

    bool databaseInstalled = false;
    WINBIO_STORAGE_SCHEMA *storageArray = NULL;
    SIZE_T storageCount = 0;

    if (SUCCEEDED(
            WinBioEnumDatabases( 
                WINBIO_TYPE_FINGERPRINT, 
                &storageArray, 
                &storageCount 
                )))
    {
        for (SIZE_T i = 0; i < storageCount; ++i)
        {
            if (storageArray[i].DatabaseId == *DatabaseId)
            {
                *DataFormat = storageArray[i].DataFormat;
                databaseInstalled = true;
                break;
            }
        }

        WinBioFree( storageArray );
        storageArray = NULL;
        storageCount = 0;
    }

    return databaseInstalled;
}
//-----------------------------------------------------------------------------
```



 

 




