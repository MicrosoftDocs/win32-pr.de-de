---
title: Durchsuchen von Binärdaten
description: Obwohl das ADSI-Suchfeature nur die Suche nach Zeichenfolgendaten unterstützt, ist es möglich, nach Binärdaten zu suchen.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Durchsuchen von Binärdaten ADSI
- Binary Data ADSI
- Binary Data ADSI , Searching Binary Data
- ADSI ADSI , Beispielcode C/C++ , Suchen nach Binärdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f77ead11f4e2d02c6e7ef3e25975a7059c2c057dbc62f71e406bbda3e24c3b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005420"
---
# <a name="searching-binary-data"></a>Durchsuchen von Binärdaten

Obwohl das ADSI-Suchfeature nur die Suche nach Zeichenfolgendaten unterstützt, ist es möglich, nach Binärdaten zu suchen. Verwenden Sie hierzu die [**ADsEncodeBinaryData-Funktion,**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) um die Binärdaten in eine Zeichenfolge zu konvertieren, die mit den Suchmethoden verwendet werden kann. Die Suche nach Binärdaten ist besonders nützlich, wenn Nach einer GUID oder SID gesucht wird, da diese Datentypen als Binärdaten gespeichert werden.

Bei Verwendung der [**ADsEncodeBinaryData-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) muss der zugeordnete Arbeitsspeicher mithilfe der [**FreeADsMem-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) freigegeben werden.

Das folgende C++-Codebeispiel zeigt, wie Sie eine Abfragezeichenfolge erstellen, um nach einem Objekt zu suchen, das über einen bestimmten **objectGUID-Wert** verfügt.


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



 

 




