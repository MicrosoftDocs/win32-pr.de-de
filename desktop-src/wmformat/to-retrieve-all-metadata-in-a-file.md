---
title: So rufen Sie alle Metadaten in einer Datei ab
description: So rufen Sie alle Metadaten in einer Datei ab
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows Medienformat-SDK, Abrufen von Metadaten
- Advanced Systems Format (ASF), Abrufen von Metadaten
- ASF (Advanced Systems Format), Abrufen von Metadaten
- Metadaten, alle abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fab81f151cbb661cc7769128e2d4371dd0b24869317d1888769ed66a60de86f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807470"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>So rufen Sie alle Metadaten in einer Datei ab

Das folgende Codebeispiel ist eine Funktion, die alle Metadaten in einer Datei anzeigt. Um die Funktion verwenden zu können, müssen Sie ihr einen Zeiger auf die [**IWMHeaderInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) eines Metadaten-Editorobjekts, Readerobjekts, synchronen Readerobjekts oder Writer-Objekts übergeben. Sie müssen auch die Stdio.h-Headerdatei an einer stelle stelle in Ihr Projekt einfügen. Weitere Informationen zur Verwendung dieses Beispiels finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)

Aus Gründen der Übersichtlichkeit werden in diesem Beispiel die Werte der Binär- und GUID-Attribute nicht angezeigt. Bei binären Attributen sollten Sie überprüfen, ob der Attributname mit einem der bekannten komplexen Metadatenattribute übereinstimmt. In diesem Falle sollten Sie die Ausgabe entsprechend der für dieses Attribut verwendeten Struktur formatieren. Auf ähnliche Weise können GUID-Attributwerte auf verschiedene Weise angezeigt werden. Sie können die einzelnen Member der Struktur einzeln anzeigen oder die Struktur in eine Zeichenfolge konvertieren und als einen Wert anzeigen.


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

 

 




