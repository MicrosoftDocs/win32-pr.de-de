---
title: Verwenden von IDirectoryObject, um eine Sicherheits Beschreibung zu erhalten
description: Dieses Thema enthält ein Codebeispiel, das verwendet wird, um eine Sicherheits Beschreibung zu erhalten.
ms.assetid: 989abd3f-9043-4c3f-a99a-63fa95daf203
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, verwenden von IDirectoryObject, um eine Sicherheits Beschreibung zu erhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 562438d37d6bfadadfee95d13f80cb4c4728e0f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724392"
---
# <a name="using-idirectoryobject-to-get-a-security-descriptor"></a><span data-ttu-id="16296-104">Verwenden von IDirectoryObject, um eine Sicherheits Beschreibung zu erhalten</span><span class="sxs-lookup"><span data-stu-id="16296-104">Using IDirectoryObject to Get a Security Descriptor</span></span>

<span data-ttu-id="16296-105">Dieses Thema enthält ein Codebeispiel, das verwendet wird, um eine Sicherheits Beschreibung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16296-105">This topic includes a code example used to get a security descriptor.</span></span>

<span data-ttu-id="16296-106">Im folgenden Codebeispiel für C++:</span><span class="sxs-lookup"><span data-stu-id="16296-106">The following C++ code example:</span></span>

-   <span data-ttu-id="16296-107">Erstellt einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="16296-107">Creates a buffer.</span></span>
-   <span data-ttu-id="16296-108">Verwendet die [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstelle, um die Sicherheits Beschreibung für das angegebene Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16296-108">Uses the [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface to get the security descriptor of the specified object.</span></span>
-   <span data-ttu-id="16296-109">Kopiert die Sicherheits Beschreibung in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="16296-109">Copies the security descriptor to the buffer.</span></span>
-   <span data-ttu-id="16296-110">Gibt einen Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) zurück, die die sicherheitsbeschreibungerdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="16296-110">Returns a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains the security descriptor data.</span></span>


```C++
HRESULT GetSDFromIDirectoryObject(
    IDirectoryObject *pObject,
    PSECURITY_DESCRIPTOR *pSecurityDescriptor)
{
    HRESULT hr = E_FAIL;
    PADS_ATTR_INFO pAttrInfo;
    DWORD dwReturn= 0;
    LPWSTR pAttrName= L"nTSecurityDescriptor";
    PSECURITY_DESCRIPTOR pSD = NULL;

    if(!pObject || !pSecurityDescriptor)
    {
        return E_INVALIDARG;
    }
 
    // Get the nTSecurityDescriptor.
    hr = pObject->GetObjectAttributes( &pAttrName, 
                                       1, 
                                       &pAttrInfo, 
                                       &dwReturn );
    if((FAILED(hr)) || (dwReturn != 1)) 
    {
        wprintf(L" failed: 0x%x\n", hr);
        return hr;
    }
 
    // Check the attribute name and type.
    if((_wcsicmp(pAttrInfo->pszAttrName,L"nTSecurityDescriptor") == 0) &&
     (pAttrInfo->dwADsType==ADSTYPE_NT_SECURITY_DESCRIPTOR))
    {
        // Get a pointer to the security descriptor.
        pSD = (PSECURITY_DESCRIPTOR)(pAttrInfo->pADsValues->SecurityDescriptor.lpValue);
               
        DWORD SDSize = pAttrInfo->pADsValues->SecurityDescriptor.dwLength;
               
        // Allocate memory for the buffer and copy the security descriptor to the buffer.
        *pSecurityDescriptor = (PSECURITY_DESCRIPTOR)CoTaskMemAlloc(SDSize);
        if (*pSecurityDescriptor)
        {
            CopyMemory((PVOID)*pSecurityDescriptor, (PVOID)pSD, SDSize);
        }
        else
        {
            hr = E_FAIL;
        }

        // Caller must free the memory for pSecurityDescriptor using CoTaskMemFree.
    }
 
    // Free memory used for the attributes retrieved.
    FreeADsMem(pAttrInfo); 
 
    return hr;
}
```



 

 