---
title: Verwenden komplexer Metadatenattribute
description: Verwenden komplexer Metadatenattribute
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows Media-Format-SDK, komplexe Metadatenattribute
- Advanced Systems Format (ASF), komplexe Metadatenattribute
- ASF (Advanced Systems Format), komplexe Metadatenattribute
- Metadaten, komplexe Attribute
- komplexe Metadatenattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd03c656a8cba5342d21e41932365455daa8bfa
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314279"
---
# <a name="using-complex-metadata-attributes"></a>Verwenden komplexer Metadatenattribute

Das Windows Media Format SDK unterstützt komplexe Metadatenattribute, bei denen es sich um Attribute mit Werten handelt, die durch eine Struktur dargestellt werden. Da alle Attribute einen Datentyp aufweisen müssen, der in der [**WMT \_ attr \_ DataType**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) -Enumeration definiert ist, werden alle komplexen Metadatenattribute als **WMT- \_ \_ typbinär Datei** behandelt. Wenn Sie ein komplexes Attribut schreiben, wandeln Sie den Zeiger in die-Struktur als Byte Zeiger um. Wenn Sie ein komplexes Attribut abrufen, wandeln Sie das [**Bytearray, das von IWMHeaderInfo3:: getattributebyindexex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) festgelegt wurde, als die entsprechende Struktur um.

In den folgenden Codebeispielen wird gezeigt, wie ein komplexes Metadatenattribut festgelegt und abgerufen wird. Mit der ersten Funktion wird ein Benutzer Text Attribut hinzugefügt, die zweite Funktion Ruft eine ab. Weitere Informationen zur Verwendung dieser Beispiele finden [Sie unter Verwenden der Code Beispiele](using-the-code-examples.md).


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

 

 




