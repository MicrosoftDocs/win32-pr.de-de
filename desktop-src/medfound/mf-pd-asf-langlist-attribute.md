---
description: Gibt eine Liste von Sprachbezeichnern an, die die in einer ASF-Datei (Advanced Systems Format) enthaltenen Sprachen angeben. Dieses Attribut entspricht dem Sprachlistenobjekt, das in der ASF-Spezifikation definiert ist.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: MF_PD_ASF_LANGLIST-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba22004001df2ba6be8fb7a173a3ea9bed1b0a73863ae111e61d36efa853e079
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119103702"
---
# <a name="mf_pd_asf_langlist-attribute"></a>MF \_ PD \_ ASF \_ LANGLIST-Attribut

Gibt eine Liste von Sprachbezeichnern an, die die in einer ASF-Datei (Advanced Systems Format) enthaltenen Sprachen angeben. Dieses Attribut entspricht dem Sprachlistenobjekt, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalt.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) erstellt den Präsentationsdeskriptor und generiert dieses Attribut aus dem Sprachlistenobjektheader. Die folgende Tabelle zeigt das Format des Blobs:



| Feld "Language List Object" | Datentyp    | Size    | Beschreibung                            |
|----------------------------|--------------|---------|----------------------------------------|
| Anzahl der Sprach-ID-Datensätze  | **DWORD**    | 4 Bytes | Anzahl der Sprachen                    |
| Sprach-ID-Datensätze        | **Byte**\[\] | Varies  | Array von Sprachzeichenfolgen (siehe unten). |



 

Das erste **DWORD** ist die Anzahl der Sprachen, gefolgt von einem Array von Sprachbezeichnerzeichenfolgen. Jede Zeichenfolge hat das folgende Format:



| Feld "Language List Object" | Datentyp     | Size    | Beschreibung                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Länge der Sprach-ID         | **DWORD**     | 4 Bytes | Die Länge der Zeichenfolge in Bytes, einschließlich der Größe des nachgestellten **NULL-Zeichens.** |
| Sprach-ID                | **Wchar**\[\] | Varies  | Eine auf NULL endende Zeichenfolge, die den RFC 1766-Sprachnamen enthält.                           |



 

Jede Zeichenfolge ist ein Sprachtag, das mit RFC 1766 kompatibel ist.

Um das Sprachtag für einen bestimmten Stream in der ASF-Datei abzurufen, fragen Sie den Streamdeskriptor nach dem [**ATTRIBUT MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE ID \_ \_ INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) ab.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie die Sprachliste analysiert wird.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

ASF-Headerobjekt
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




