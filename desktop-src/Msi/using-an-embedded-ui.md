---
description: Eine benutzerdefinierte Benutzeroberfläche kann in das Windows Installer Paket eingebettet werden.
ms.assetid: d037cd8d-9c88-4851-a9da-b2179f53cee6
title: Verwenden einer eingebetteten Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f187e50461cfe88adc9c2cabbf8dd8b88ca97a5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104050743"
---
# <a name="using-an-embedded-ui"></a><span data-ttu-id="f36ab-103">Verwenden einer eingebetteten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f36ab-103">Using an Embedded UI</span></span>

<span data-ttu-id="f36ab-104">Eine benutzerdefinierte Benutzeroberfläche kann in das Windows Installer Paket eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="f36ab-104">A custom user interface can be embedded within the Windows Installer package.</span></span>

<span data-ttu-id="f36ab-105">Die DLL-Datei, die die benutzerdefinierte Benutzeroberfläche und alle von der benutzerdefinierten Benutzeroberfläche verwendeten Ressourcen Dateien enthält, sollte in der Tabelle [msiembeddedui](msiembeddedui-table.md) aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f36ab-105">The DLL file containing the custom UI, and any resource files used by the custom UI, should be listed in the [MsiEmbeddedUI](msiembeddedui-table.md) table.</span></span> <span data-ttu-id="f36ab-106">Diese msiembeddedui-Tabelle enthält beispielsweise eine Zeile für die DLL-Datei, die die eingebettete Benutzeroberfläche enthält, und eine Zeile für eine Bitmapdatei, die von der Benutzeroberfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f36ab-106">For example, this MsiEmbeddedUI table contains a row for the DLL file containing the embedded UI and a row for a bitmap file used by the UI.</span></span>

| <span data-ttu-id="f36ab-107">Msiembeddedui</span><span class="sxs-lookup"><span data-stu-id="f36ab-107">MsiEmbeddedUI</span></span> | <span data-ttu-id="f36ab-108">FileName</span><span class="sxs-lookup"><span data-stu-id="f36ab-108">FileName</span></span>    | <span data-ttu-id="f36ab-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="f36ab-109">Attributes</span></span> | <span data-ttu-id="f36ab-110">MessageFilter</span><span class="sxs-lookup"><span data-stu-id="f36ab-110">MessageFilter</span></span> | <span data-ttu-id="f36ab-111">Daten</span><span class="sxs-lookup"><span data-stu-id="f36ab-111">Data</span></span>            |
|---------------|-------------|------------|---------------|-----------------|
| <span data-ttu-id="f36ab-112">Embeddedui</span><span class="sxs-lookup"><span data-stu-id="f36ab-112">EmbeddedUI</span></span>    | <span data-ttu-id="f36ab-113">embedui.dll</span><span class="sxs-lookup"><span data-stu-id="f36ab-113">embedui.dll</span></span> | <span data-ttu-id="f36ab-114">3</span><span class="sxs-lookup"><span data-stu-id="f36ab-114">3</span></span>          | <span data-ttu-id="f36ab-115">201359327</span><span class="sxs-lookup"><span data-stu-id="f36ab-115">201359327</span></span>     | <span data-ttu-id="f36ab-116">\[Binärdaten\]</span><span class="sxs-lookup"><span data-stu-id="f36ab-116">\[Binary Data\]</span></span> |
| <span data-ttu-id="f36ab-117">Custombitmap</span><span class="sxs-lookup"><span data-stu-id="f36ab-117">CustomBitmap</span></span>  | <span data-ttu-id="f36ab-118">custom.bmp</span><span class="sxs-lookup"><span data-stu-id="f36ab-118">custom.bmp</span></span>  | <span data-ttu-id="f36ab-119">0</span><span class="sxs-lookup"><span data-stu-id="f36ab-119">0</span></span>          |               | <span data-ttu-id="f36ab-120">\[Binärdaten\]</span><span class="sxs-lookup"><span data-stu-id="f36ab-120">\[Binary Data\]</span></span> |



 

<span data-ttu-id="f36ab-121">In diesem Beispiel embedui.dll die benutzerdefinierte UI-dll die benutzerdefinierten *initializeembeddedui*-, *embeddeduihandler*-und *shutdownembeddedui* -Funktionen exportieren.</span><span class="sxs-lookup"><span data-stu-id="f36ab-121">The custom UI DLL, in this example embedui.dll, should export the user-defined *InitializeEmbeddedUI*, *EmbeddedUIHandler*, and *ShutdownEmbeddedUI* functions.</span></span> <span data-ttu-id="f36ab-122">Der folgende Beispielcode veranschaulicht diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f36ab-122">The following sample code illustrates these functions.</span></span>


```C++
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <msi.h>
#include <msiquery.h>
#include <Aclapi.h>
#include <strsafe.h>
#pragma comment(lib, "msi.lib")

#define cchGUID 38

int __stdcall InitializeEmbeddedUI(MSIHANDLE hInstall, 
        LPCWSTR szResourcePath, LPDWORD pdwInternalUILevel)
{
    // The hInstall handle is only valid within this function and 
     // can be used to get or set properties. The handle 
    // does not need to be explicitly closed.

    WCHAR szProductCode[cchGUID+1];
    DWORD cchProductCode = ARRAYSIZE(szProductCode);
    UINT uiStat =  MsiGetProperty(hInstall, L"ProductCode",
             szProductCode, &cchProductCode);
    UNREFERENCED_PARAMETER(szResourcePath);

    if (ERROR_SUCCESS != uiStat)
    {
        // The installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    WCHAR* szReinstall = NULL;
    DWORD cchReinstall = 0;
    uiStat = MsiGetProperty(hInstall, TEXT("REINSTALL"),  
            szReinstall, &cchReinstall);
    if (ERROR_MORE_DATA == uiStat)
    {
        ++cchProductCode; // Add 1 for terminating null character.
        szReinstall = new WCHAR[cchReinstall];
        if (szReinstall)
        {
        uiStat = MsiGetProperty(hInstall, L"REINSTALL", 
                szReinstall, &cchReinstall);
        }
    }
    if (ERROR_SUCCESS != uiStat)
    {
        if (szReinstall != NULL) 
            delete [] szReinstall;
        // This installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    if (INSTALLSTATE_DEFAULT != MsiQueryProductState(szProductCode))
    {
        if (INSTALLUILEVEL_BASIC == *pdwInternalUILevel)
        {
            // Insert the custom UI used by basic installation here.
        }
        else
        {
            // Insert the custom UI used by full installation here.
        }
    }
    else if (szReinstall && szReinstall[0])
    {
        // Reinstall the UI sequence.
    }
    else
    {
        // This is a maintenance installation. Remove the UI sequence.

        MsiSetProperty(hInstall, TEXT("REMOVE"), TEXT("ALL"));
    }

    if (szProductCode)
        delete [] szReinstall;

    // Setting the internal UI level to none specifies that 
    // no authored UI should run.
    *pdwInternalUILevel = INSTALLUILEVEL_NONE;
    return 0;
}

DWORD __stdcall ShutdownEmbeddedUI()
{
    // ShutdownEmbeddedUI is optional. It can allow the embedded UI 
    // to perform any cleanup. After this call, the embedded UI   
    // should not receive any additional callbacks.
    return 0;
}


INT __stdcall EmbeddedUIHandler(UINT iMessageType, MSIHANDLE hRecord)
{
    // This function is similar to the MsiSetExternalUIRecord callback.
    INSTALLMESSAGE mt;
    UINT uiFlags;
    UNREFERENCED_PARAMETER(hRecord);

    mt = (INSTALLMESSAGE) (0xFF000000 & (UINT) iMessageType);
    uiFlags = 0x00FFFFFF & iMessageType;

    switch (mt)
    {
    case INSTALLMESSAGE_FATALEXIT:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ERROR:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_WARNING:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_FILESINUSE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_RESOLVESOURCE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_USER:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INFO:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_OUTOFDISKSPACE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONSTART:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_PROGRESS:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_SHOWDIALOG:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_COMMONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLSTART:
        {
            // This message is sent when the Install begins.
            // Record contains the ProductName and ProductCode
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLEND:
        {
            // This message is sent when the Install ends.
            // Record contains the ProductName and ProductCode 
            // and return value of the installation.
            return IDOK;
        }

    default:
        {
            return 0;
        }
    }
}
```



 

 



