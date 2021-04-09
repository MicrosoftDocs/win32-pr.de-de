---
title: Suchen von Binärdaten
description: Obwohl die ADSI-Suchfunktion nur das Suchen nach Zeichen folgen Daten unterstützt, ist es möglich, Binärdaten zu suchen.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Suchen von Binärdaten ADSI
- Binäre Daten (ADSI)
- Binary Data ADSI, Durchsuchen von Binärdaten
- ADSI ADSI, Beispiel Code C/C++, suchen nach Binärdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036305"
---
# <a name="searching-binary-data"></a><span data-ttu-id="851a3-107">Suchen von Binärdaten</span><span class="sxs-lookup"><span data-stu-id="851a3-107">Searching Binary Data</span></span>

<span data-ttu-id="851a3-108">Obwohl die ADSI-Suchfunktion nur das Suchen nach Zeichen folgen Daten unterstützt, ist es möglich, Binärdaten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="851a3-108">Even though the ADSI search feature only supports searching for string data, it is possible to search for binary data.</span></span> <span data-ttu-id="851a3-109">Verwenden Sie hierzu die [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) -Funktion, um die Binärdaten in eine Zeichenfolge zu konvertieren, die mit den Suchmethoden verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="851a3-109">To do this, use the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function to convert the binary data into a string that can be used with the search methods.</span></span> <span data-ttu-id="851a3-110">Das Suchen nach Binärdaten ist besonders nützlich, wenn Sie nach einer GUID oder einer SID suchen, da diese Datentypen als Binärdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="851a3-110">Searching for binary data is particularly useful when searching for a GUID or a SID because these data types are stored as binary data.</span></span>

<span data-ttu-id="851a3-111">Bei Verwendung der [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) -Funktion muss der zugeordnete Arbeitsspeicher mithilfe der Funktion " [**freadsmem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) " freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="851a3-111">When using the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function, the memory allocated must be freed using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="851a3-112">Im folgenden C++-Codebeispiel wird gezeigt, wie eine Abfrage Zeichenfolge erstellt wird, um nach einem Objekt zu suchen, das einen bestimmten **objectGUID** -Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="851a3-112">The following C++ code example shows how to build a query string to search for an object that has a particular **objectGUID** value.</span></span>


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 




