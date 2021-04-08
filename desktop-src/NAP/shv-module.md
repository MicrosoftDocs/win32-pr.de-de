---
title: SHV-Modul
description: Hinweis die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht mehr verfügbar. es wird ein SHV-Modul (System Health Prüfungs) eingerichtet, einschließlich Registrierung und Aufhebung der Registrierung beim NAP-System.
ms.assetid: 0f2edd23-d44a-4a01-ae33-f7eef0e4b27f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95784d05f4bf377f356a91fe5b0c1811fb9671d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709797"
---
# <a name="shv-module"></a><span data-ttu-id="0b57b-103">SHV-Modul</span><span class="sxs-lookup"><span data-stu-id="0b57b-103">SHV Module</span></span>

> [!Note]  
> <span data-ttu-id="0b57b-104">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0b57b-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0b57b-105">Richtet ein SHV-Modul (System Health Prüfungs) ein, einschließlich Registrierung und Aufhebung der Registrierung beim NAP-System.</span><span class="sxs-lookup"><span data-stu-id="0b57b-105">Sets up a system health validator (SHV) module including registration and unregistration with the NAP system.</span></span>

> [!Note]  
> <span data-ttu-id="0b57b-106">Das NAP-SDK enthält außerdem einen vollständigen Satz von Beispielcode, der sich im... \\ Beispiele für \\ netds- \\ NAP... Verzeichnis der SDK-Installation.</span><span class="sxs-lookup"><span data-stu-id="0b57b-106">The NAP SDK also contains a full set of sample code that can be found in the ...\\Samples\\NetDS\\NAP... directory of your SDK installation.</span></span> <span data-ttu-id="0b57b-107">Diese Beispiel Gruppe enthält einen Systemintegritäts-Agent (SHA), SHV und einen Erzwingungs Client (EC).</span><span class="sxs-lookup"><span data-stu-id="0b57b-107">This sample set includes a system health agent (SHA), SHV, and enforcement client (EC).</span></span> <span data-ttu-id="0b57b-108">Es verfügt über vollständige funktionierende NAP-Szenarien zum Einrichten der Kommunikation zwischen SHA-SHV und SHA-ec.</span><span class="sxs-lookup"><span data-stu-id="0b57b-108">It has full working NAP scenarios setting up communication between SHA-SHV and SHA-EC.</span></span>

 


```C++
#include <windows.h>
#include "stdafx.h"
#include "NapUtil.h"

static const wchar_t friendlyName[] = L"SDK SHV Sample";
static const wchar_t version[] = L"1.0.0.1";
static const wchar_t description[] = L"System Health Validator(SHV)";
static const wchar_t vendor[] = L"Microsoft";

/// Registers the SDK SHV with the NAP Server.
HRESULT RegisterSdkShv()
{
    HRESULT hr = S_OK;
    CComPtr<INapServerManagement> pSHVMgmt = NULL;
    
    NapComponentRegistrationInfo shvInfo;
    ZeroMemory (&shvInfo, sizeof(shvInfo));

    hr = pSHVMgmt.CoCreateInstance(CLSID_NapServerManagement, NULL, CLSCTX_INPROC_SERVER);
    hr = FillShvComponentRegistrationInfo(&shvInfo);
    hr = pSHVMgmt->RegisterSystemHealthValidator(&shvInfo, (CLSID *)&__uuidof(CSampleShv));
    
    FreeComponentRegistration(&shvInfo);
    return hr;
}

/// Unregisters the SDK SHV with the NAP Server.
HRESULT UnregisterSdkShv()
{
    HRESULT hr = S_OK;
    CComPtr<INapServerManagement> pSHVMgmt = NULL;

    hr = pSHVMgmt.CoCreateInstance(CLSID_NapServerManagement, NULL, CLSCTX_INPROC_SERVER);
    hr = pSHVMgmt->UnregisterSystemHealthValidator(QuarSampleSystemHealthId);
    return hr;
}

/// Fill the NapComponentRegistrationInfo structure that needs to be passed during registration.
HRESULT FillShvComponentRegistrationInfo (NapComponentRegistrationInfo *shvInfo)
{
    HRESULT hr = S_OK;
    shvInfo->id = QuarSampleSystemHealthId;

    //<Temporarily till implement the Info Class>
    shvInfo->infoClsid = GUID_NULL; 

    hr = ConstructCountedString(friendlyName, sizeof(friendlyName), &(shvInfo->friendlyName));
    hr = ConstructCountedString(description, sizeof(description), &(shvInfo->description));
    hr = ConstructCountedString(version, sizeof(version), &(shvInfo->version));
    hr = ConstructCountedString(vendor, sizeof(vendor), &(shvInfo->vendorName));
    return hr;
}

// Helper Function for FillShvComponentRegistrationInfo.
HRESULT ConstructCountedString(const WCHAR* src, UINT16 len, CountedString* dest)
{
    HRESULT hr = S_OK;
    DWORD retCode = ERROR_SUCCESS;
    hr = AllocateMemory(dest->string, ((len+1)*sizeof(WCHAR)));
    dest->length = len;
    retCode = StringCchCopy(dest->string, len+1, src);
    return hr;
}

// Helper Function for releasing ShaComponentRegistrationInfo members
void FreeComponentRegistration(NapComponentRegistrationInfo *shvInfo)
{
    FreeMemory(shvInfo->friendlyName.string);
    FreeMemory(shvInfo->description.string);
    FreeMemory(shvInfo->version.string);
    FreeMemory(shvInfo->vendorName.string);
}

```



 

 




