---
title: So rufen Sie alle Metadaten in einer Datei ab
description: So rufen Sie alle Metadaten in einer Datei ab
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows Media-Format-SDK, Abrufen von Metadaten
- Advanced Systems Format (ASF), Abrufen von Metadaten
- ASF (Advanced Systems Format), Abrufen von Metadaten
- Metadaten, Abrufen aller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc5d63a27cd4455d8d39cebee894dfbfc8d5bf2c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341913"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>So rufen Sie alle Metadaten in einer Datei ab

Das folgende Codebeispiel ist eine Funktion, mit der alle Metadaten in einer Datei angezeigt werden. Um die-Funktion zu verwenden, müssen Sie Ihr einen Zeiger auf die [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle eines Metadaten-Editor-Objekts, eines Reader-Objekts, eines synchronen Reader-Objekts oder eines Writer-Objekts übergeben. Sie müssen auch die Header Datei "stdio. h" an einer beliebigen Stelle in Ihrem Projekt einschließen. Weitere Informationen zur Verwendung dieses Beispiels finden [Sie unter Verwenden der Code Beispiele](using-the-code-examples.md).

Aus Gründen der Übersichtlichkeit werden in diesem Beispiel die Werte von Binary-und GUID-Attributen nicht angezeigt. Für binäre Attribute sollten Sie überprüfen, ob der Attribut Name mit einem der bekannten komplexen Metadatenattribute übereinstimmt. Wenn dies der Fall ist, sollten Sie die Ausgabe entsprechend der für dieses Attribut verwendeten Struktur formatieren. Ebenso können GUID-Attributwerte auf verschiedene Weise angezeigt werden. Sie können jeden Member der Struktur einzeln anzeigen oder die Struktur in eine Zeichenfolge konvertieren und als einen Wert anzeigen.


```C++
HRESULT ShowAllAttributes(IWMHeaderInfo3* pHeaderInfo)
{
    HRESULT hr          = S_OK;
    
    WORD    cAttributes = 0;
    WCHAR*  pwszName    = NULL;
    WORD    cchName     = 0;
    BYTE*   pbValue     = NULL;
    DWORD   cbValue     = 0;
    WORD    langIndex   = 0;
    WORD    attIndex    = 0;

    WMT_ATTR_DATATYPE attType;

    // Get the total number of attributes in the file.

    hr = pHeaderInfo->GetAttributeCountEx(0xFFFF, &cAttributes);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all the attributes, retrieving and displaying each.

    for(attIndex = 0; attIndex < cAttributes; attIndex++)
    {
        // Get the required buffer lengths for the name and value.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                NULL,
                                                &cchName,
                                                NULL,
                                                NULL,
                                                NULL,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate the buffers.

        pwszName = new WCHAR[cchName];
        if(pwszName == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        pbValue = new BYTE[cbValue];
        if(pbValue == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the attribute.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                pwszName,
                                                &cchName,
                                                &attType,
                                                &langIndex,
                                                pbValue,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Display the attribute global index and name.

        printf("%3d - %S (Language %d):\n\t ", attIndex, pwszName, langIndex);

        // Display the attribute depending upon type.

        switch(attType)
        {
        case WMT_TYPE_DWORD:
        case WMT_TYPE_QWORD:
        case WMT_TYPE_WORD:
            printf("%d\n\n", (DWORD) *pbValue);
            break;
        case WMT_TYPE_STRING:
            printf("%S\n\n", (WCHAR*) pbValue);
            break;
        case WMT_TYPE_BINARY:
            printf("<binary value>\n\n");
            break;
        case WMT_TYPE_BOOL:
            printf("%s\n\n", ((BOOL) *pbValue == TRUE) ? "True" : "False");
            break;
        case WMT_TYPE_GUID:
            printf("<GUID value>\n\n", (DWORD) *pbValue);
            break;
        }

        // Release allocated memory for the next pass.

        SAFE_ARRAY_DELETE(pwszName);
        SAFE_ARRAY_DELETE(pbValue);
        cchName = 0;
        cbValue = 0;
    } // End for attIndex.

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Abrufen von Metadatenattributen**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




