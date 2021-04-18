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
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="6f87a-104">MF \_ PD, \_ ASF \_ langlist-Attribut</span><span class="sxs-lookup"><span data-stu-id="6f87a-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="6f87a-105">Gibt eine Liste von sprach Bezeichnerzeichen an, die die in einer ASF-Datei (Advanced Systems Format) enthaltenen Sprachen angibt.</span><span class="sxs-lookup"><span data-stu-id="6f87a-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="6f87a-106">Dieses Attribut entspricht dem sprach Listen Objekt, das in der ASF-Spezifikation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6f87a-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f87a-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6f87a-107">Data type</span></span>

<span data-ttu-id="6f87a-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="6f87a-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="6f87a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f87a-109">Remarks</span></span>

<span data-ttu-id="6f87a-110">Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="6f87a-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="6f87a-111">Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode erstellt den Präsentations Deskriptor und generiert dieses Attribut aus dem sprach Listen Objekt-Header.</span><span class="sxs-lookup"><span data-stu-id="6f87a-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="6f87a-112">In der folgenden Tabelle wird das Format des BLOBs angezeigt:</span><span class="sxs-lookup"><span data-stu-id="6f87a-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="6f87a-113">Feld "sprach Listen Objekt"</span><span class="sxs-lookup"><span data-stu-id="6f87a-113">Language List Object field</span></span> | <span data-ttu-id="6f87a-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6f87a-114">Data type</span></span>    | <span data-ttu-id="6f87a-115">Size</span><span class="sxs-lookup"><span data-stu-id="6f87a-115">Size</span></span>    | <span data-ttu-id="6f87a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f87a-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="6f87a-117">Anzahl der Sprach-ID-Einträge</span><span class="sxs-lookup"><span data-stu-id="6f87a-117">Language ID Records Count</span></span>  | <span data-ttu-id="6f87a-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="6f87a-118">**DWORD**</span></span>    | <span data-ttu-id="6f87a-119">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="6f87a-119">4 bytes</span></span> | <span data-ttu-id="6f87a-120">Anzahl von Sprachen</span><span class="sxs-lookup"><span data-stu-id="6f87a-120">Number of languages</span></span>                    |
| <span data-ttu-id="6f87a-121">Sprach-ID-Einträge</span><span class="sxs-lookup"><span data-stu-id="6f87a-121">Language ID Records</span></span>        | <span data-ttu-id="6f87a-122">**Hobby**\[\]</span><span class="sxs-lookup"><span data-stu-id="6f87a-122">**BYTE**\[\]</span></span> | <span data-ttu-id="6f87a-123">Varies</span><span class="sxs-lookup"><span data-stu-id="6f87a-123">Varies</span></span>  | <span data-ttu-id="6f87a-124">Array von sprach Zeichenfolgen (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="6f87a-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="6f87a-125">Der erste **DWORD** -Wert ist die Anzahl der Sprachen, gefolgt von einem Array von sprachbezeichnerzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6f87a-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="6f87a-126">Jede Zeichenfolge weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="6f87a-126">Each string has the following format:</span></span>



| <span data-ttu-id="6f87a-127">Feld "sprach Listen Objekt"</span><span class="sxs-lookup"><span data-stu-id="6f87a-127">Language List Object field</span></span> | <span data-ttu-id="6f87a-128">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6f87a-128">Data type</span></span>     | <span data-ttu-id="6f87a-129">Size</span><span class="sxs-lookup"><span data-stu-id="6f87a-129">Size</span></span>    | <span data-ttu-id="6f87a-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f87a-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f87a-131">Länge der Sprach-ID</span><span class="sxs-lookup"><span data-stu-id="6f87a-131">Language ID Length</span></span>         | <span data-ttu-id="6f87a-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="6f87a-132">**DWORD**</span></span>     | <span data-ttu-id="6f87a-133">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="6f87a-133">4 bytes</span></span> | <span data-ttu-id="6f87a-134">Die Länge der Zeichenfolge in Bytes, einschließlich der Größe des nachfolgenden **null** Zeichens.</span><span class="sxs-lookup"><span data-stu-id="6f87a-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="6f87a-135">Sprach-ID</span><span class="sxs-lookup"><span data-stu-id="6f87a-135">Language ID</span></span>                | <span data-ttu-id="6f87a-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="6f87a-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="6f87a-137">Varies</span><span class="sxs-lookup"><span data-stu-id="6f87a-137">Varies</span></span>  | <span data-ttu-id="6f87a-138">Eine mit NULL endenden Zeichenfolge, die den Namen der RFC 1766-Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="6f87a-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="6f87a-139">Jede Zeichenfolge ist ein sprach Kennzeichen, das mit RFC 1766 kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="6f87a-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="6f87a-140">Um das Sprachtag für einen bestimmten Datenstrom in der ASF-Datei zu erhalten, Fragen Sie den Datenstrom Deskriptor nach dem Attribut "MF SD-ID-Attribut für die [**\_ sprach- \_ \_ \_ \_ ID \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) " ab.</span><span class="sxs-lookup"><span data-stu-id="6f87a-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6f87a-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f87a-141">Examples</span></span>

<span data-ttu-id="6f87a-142">Im folgenden Beispiel wird gezeigt, wie die-Sprachliste analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="6f87a-142">The following example shows how to parse the language list.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6f87a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f87a-143">Requirements</span></span>



| <span data-ttu-id="6f87a-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f87a-144">Requirement</span></span> | <span data-ttu-id="6f87a-145">Wert</span><span class="sxs-lookup"><span data-stu-id="6f87a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f87a-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f87a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6f87a-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f87a-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6f87a-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f87a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6f87a-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f87a-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6f87a-150">Header</span><span class="sxs-lookup"><span data-stu-id="6f87a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f87a-151"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f87a-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f87a-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f87a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f87a-153">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6f87a-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f87a-154">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6f87a-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6f87a-155">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="6f87a-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6f87a-156">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="6f87a-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="6f87a-157">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="6f87a-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f87a-158">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="6f87a-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="6f87a-159">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="6f87a-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="6f87a-160">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="6f87a-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




