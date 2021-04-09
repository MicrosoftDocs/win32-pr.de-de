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
# <a name="searching-binary-data"></a>Suchen von Binärdaten

Obwohl die ADSI-Suchfunktion nur das Suchen nach Zeichen folgen Daten unterstützt, ist es möglich, Binärdaten zu suchen. Verwenden Sie hierzu die [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) -Funktion, um die Binärdaten in eine Zeichenfolge zu konvertieren, die mit den Suchmethoden verwendet werden kann. Das Suchen nach Binärdaten ist besonders nützlich, wenn Sie nach einer GUID oder einer SID suchen, da diese Datentypen als Binärdaten gespeichert werden.

Bei Verwendung der [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) -Funktion muss der zugeordnete Arbeitsspeicher mithilfe der Funktion " [**freadsmem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) " freigegeben werden.

Im folgenden C++-Codebeispiel wird gezeigt, wie eine Abfrage Zeichenfolge erstellt wird, um nach einem Objekt zu suchen, das einen bestimmten **objectGUID** -Wert aufweist.


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



 

 




