---
title: Beispielcode zum Erstellen einer bindbaren Zeichenfolgendarstellung einer GUID
description: Das folgende Codebeispiel kann verwendet werden, um eine Zeichenfolgendarstellung einer GUID zurückgibt, die zum Binden an das -Objekt verwendet werden kann.
ms.assetid: e39a6994-4328-40f2-8cb5-8b1f971e50d8
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Erstellen einer bindbaren Zeichenfolgendarstellung einer GUID'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2baafefa712d8826b5fc9442e1da8aaeac54d58c1e491750b2d39ceb5ee88ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694283"
---
# <a name="example-code-for-creating-a-bindable-string-representation-of-a-guid"></a>Beispielcode zum Erstellen einer bindbaren Zeichenfolgendarstellung einer GUID

Das folgende Codebeispiel kann verwendet werden, um eine Zeichenfolgendarstellung einer GUID zurückgibt, die zum Binden an das -Objekt verwendet werden kann.


```C++
//*******************************************************************
//
//  GUIDtoBindableString()
//
//  Converts a GUID into a string that can be used for binding with  
//  the <GUID= or <WKGUID= syntax. The caller must free the allocated  
//  string with the FreeADsStr when it is no longer required.
//
//*******************************************************************

HRESULT GUIDtoBindableString(LPGUID pGUID, LPWSTR *ppGUIDString)
{
    if((!pGUID) || (ppGUIDString==NULL))
    {
        return E_INVALIDARG;
    }

    // Build bindable GUID string.
    DWORD dwBytes =  sizeof(GUID);
    WCHAR szByte[3];
    LPWSTR pwszGUID = new WCHAR[(dwBytes * 2) + 1];
    if(NULL == pwszGUID)
    {
        return E_OUTOFMEMORY;
    }

    *pwszGUID = NULL;

    HRESULT hr = S_OK;
    LPBYTE lpByte;
    DWORD dwItem;

    // Loop through to add each byte to the string.
    for(dwItem = 0, 
        lpByte = (LPBYTE)pGUID; dwItem < dwBytes; 
        dwItem++)
    {
        // Append to pwszGUID, double-byte, byte at dwItem index.
        swprintf_s(szByte, L"%02x", lpByte[dwItem]);
        wcscat_s(pwszGuid, szByte);
    }
    
    // Allocate memory for the string.
    *ppGUIDString = AllocADsStr(pwszGUID);

    delete [] pwszGUID;
    
    if(NULL != *ppGUIDString)
    {
        hr = S_OK;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    
    // Caller must free ppGUIDString using FreeADsStr.
    return hr;
}
```



 

 




