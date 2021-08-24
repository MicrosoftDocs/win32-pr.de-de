---
title: Verwenden komplexer Metadatenattribute
description: Verwenden komplexer Metadatenattribute
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows Medienformat-SDK, komplexe Metadatenattribute
- Advanced Systems Format (ASF), komplexe Metadatenattribute
- ASF (Advanced Systems Format), komplexe Metadatenattribute
- Metadaten, komplexe Attribute
- Komplexe Metadatenattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8245d2fbc07878a73e304cfc573e05e93b605185ece93655dae7a8bdeff0d9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807250"
---
# <a name="using-complex-metadata-attributes"></a>Verwenden komplexer Metadatenattribute

Das Windows Media Format SDK unterstützt komplexe Metadatenattribute, bei denen es sich um Attribute handelt, deren Werte von einer -Struktur dargestellt werden. Da alle Attribute über einen in der [**WMT \_ ATTR \_ DATATYPE-Enumeration**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) definierten Datentyp verfügen müssen, werden alle komplexen Metadatenattribute als **WMT \_ TYPE \_ BINARY** behandelt. Wenn Sie ein komplexes Attribut schreiben, casten Sie den Zeiger in die -Struktur als Bytezeiger. Wenn Sie ein komplexes Attribut abrufen, legen Sie das by [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) festgelegte Bytearray in die entsprechende Struktur um.

Die folgenden Codebeispiele zeigen, wie Sie ein komplexes Metadatenattribut festlegen und abrufen. Die erste Funktion fügt ein Benutzertextattribut hinzu, die zweite Funktion ruft eins ab. Weitere Informationen zur Verwendung dieser Beispiele finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




