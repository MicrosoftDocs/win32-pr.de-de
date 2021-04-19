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
# <a name="to-retrieve-all-metadata-in-a-file"></a><span data-ttu-id="645ec-107">So rufen Sie alle Metadaten in einer Datei ab</span><span class="sxs-lookup"><span data-stu-id="645ec-107">To Retrieve All Metadata in a File</span></span>

<span data-ttu-id="645ec-108">Das folgende Codebeispiel ist eine Funktion, mit der alle Metadaten in einer Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="645ec-108">The following code example is a function that displays all the metadata in a file.</span></span> <span data-ttu-id="645ec-109">Um die-Funktion zu verwenden, müssen Sie Ihr einen Zeiger auf die [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle eines Metadaten-Editor-Objekts, eines Reader-Objekts, eines synchronen Reader-Objekts oder eines Writer-Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="645ec-109">In order to use the function, you must pass it a pointer to the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface of a metadata editor object, reader object, synchronous reader object, or writer object.</span></span> <span data-ttu-id="645ec-110">Sie müssen auch die Header Datei "stdio. h" an einer beliebigen Stelle in Ihrem Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="645ec-110">You must also include the Stdio.h header file somewhere in your project.</span></span> <span data-ttu-id="645ec-111">Weitere Informationen zur Verwendung dieses Beispiels finden [Sie unter Verwenden der Code Beispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="645ec-111">For more information about how to use this example, see [Using the Code Examples](using-the-code-examples.md).</span></span>

<span data-ttu-id="645ec-112">Aus Gründen der Übersichtlichkeit werden in diesem Beispiel die Werte von Binary-und GUID-Attributen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="645ec-112">For clarity, this example does not display the values of binary and GUID attributes.</span></span> <span data-ttu-id="645ec-113">Für binäre Attribute sollten Sie überprüfen, ob der Attribut Name mit einem der bekannten komplexen Metadatenattribute übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="645ec-113">For binary attributes, you should check to see if the attribute name matches any of the known complex metadata attributes.</span></span> <span data-ttu-id="645ec-114">Wenn dies der Fall ist, sollten Sie die Ausgabe entsprechend der für dieses Attribut verwendeten Struktur formatieren.</span><span class="sxs-lookup"><span data-stu-id="645ec-114">If it does, you should format your output according to the structure used for that attribute.</span></span> <span data-ttu-id="645ec-115">Ebenso können GUID-Attributwerte auf verschiedene Weise angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="645ec-115">Similarly, GUID attribute values can be displayed in a number of ways.</span></span> <span data-ttu-id="645ec-116">Sie können jeden Member der Struktur einzeln anzeigen oder die Struktur in eine Zeichenfolge konvertieren und als einen Wert anzeigen.</span><span class="sxs-lookup"><span data-stu-id="645ec-116">You can choose to display each member of the structure one at a time or convert the structure to a string and display it as one value.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="645ec-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="645ec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="645ec-118">**Abrufen von Metadatenattributen**</span><span class="sxs-lookup"><span data-stu-id="645ec-118">**Retrieving Metadata Attributes**</span></span>](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




