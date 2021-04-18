---
description: Gibt eine Liste von sprach Bezeichnerzeichen an, die die in einer ASF-Datei (Advanced Systems Format) enthaltenen Sprachen angibt. Dieses Attribut entspricht dem sprach Listen Objekt, das in der ASF-Spezifikation definiert ist.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: MF_PD_ASF_LANGLIST-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351802"
---
# <a name="mf_pd_asf_langlist-attribute"></a>MF \_ PD, \_ ASF \_ langlist-Attribut

Gibt eine Liste von sprach Bezeichnerzeichen an, die die in einer ASF-Datei (Advanced Systems Format) enthaltenen Sprachen angibt. Dieses Attribut entspricht dem sprach Listen Objekt, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem sprach Listen Objekt-Header. In der folgenden Tabelle wird das Format des BLOBs angezeigt:



| Feld "sprach Listen Objekt" | Datentyp    | Size    | BESCHREIBUNG                            |
|----------------------------|--------------|---------|----------------------------------------|
| Anzahl der Sprach-ID-Einträge  | **DWORD**    | 4 Bytes | Anzahl von Sprachen                    |
| Sprach-ID-Einträge        | **Hobby**\[\] | Varies  | Array von sprach Zeichenfolgen (siehe unten). |



 

Der erste **DWORD** -Wert ist die Anzahl der Sprachen, gefolgt von einem Array von sprachbezeichnerzeichenfolgen. Jede Zeichenfolge weist das folgende Format auf:



| Feld "sprach Listen Objekt" | Datentyp     | Size    | BESCHREIBUNG                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Länge der Sprach-ID         | **DWORD**     | 4 Bytes | Die Länge der Zeichenfolge in Bytes, einschließlich der Größe des nachfolgenden **null** Zeichens. |
| Sprach-ID                | **WCHAR**\[\] | Varies  | Eine mit NULL endenden Zeichenfolge, die den Namen der RFC 1766-Sprache enthält.                           |



 

Jede Zeichenfolge ist ein sprach Kennzeichen, das mit RFC 1766 kompatibel ist.

Um das Sprachtag für einen bestimmten Datenstrom in der ASF-Datei zu erhalten, Fragen Sie den Datenstrom Deskriptor nach dem Attribut "MF SD-ID-Attribut für die [**\_ sprach- \_ \_ \_ \_ ID \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) " ab.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die-Sprachliste analysiert wird.


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

ASF-Header Objekt
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




