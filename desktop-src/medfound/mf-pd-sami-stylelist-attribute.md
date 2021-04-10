---
description: Enthält die anzeigen amen der in der Sami-Datei definierten Sami-Stile (in der Datei mit synchroner Barrierefreiheit).
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868547"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="7ff1a-103">MF \_ PD, \_ Sami \_ stylelist-Attribut</span><span class="sxs-lookup"><span data-stu-id="7ff1a-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="7ff1a-104">Enthält die anzeigen amen der in der Sami-Datei definierten Sami-Stile (in der Datei mit synchroner Barrierefreiheit).</span><span class="sxs-lookup"><span data-stu-id="7ff1a-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="7ff1a-105">Die [Sami Media-Quelle](sami-media-source.md) legt dieses Attribut auf dem Präsentations Deskriptor fest, den Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ff1a-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7ff1a-106">Data type</span></span>

<span data-ttu-id="7ff1a-107">Bytearray</span><span class="sxs-lookup"><span data-stu-id="7ff1a-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff1a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ff1a-108">Remarks</span></span>

<span data-ttu-id="7ff1a-109">Das Attribut-BLOB weist die folgende Struktur auf:</span><span class="sxs-lookup"><span data-stu-id="7ff1a-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="7ff1a-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7ff1a-110">Data Type</span></span>

<span data-ttu-id="7ff1a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ff1a-111">Description</span></span>

<span data-ttu-id="7ff1a-112">Größe (Byte)</span><span class="sxs-lookup"><span data-stu-id="7ff1a-112">Size (bytes)</span></span>

<span data-ttu-id="7ff1a-113">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7ff1a-113">**DWORD**</span></span>

<span data-ttu-id="7ff1a-114">Anzahl von Format Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-114">Number of style strings.</span></span>

<span data-ttu-id="7ff1a-115">4</span><span class="sxs-lookup"><span data-stu-id="7ff1a-115">4</span></span>

<span data-ttu-id="7ff1a-116">Für jede Format Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="7ff1a-116">For each style string:</span></span>

<span data-ttu-id="7ff1a-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7ff1a-117">**DWORD**</span></span>

<span data-ttu-id="7ff1a-118">Größe der Zeichenfolge in Bytes, einschließlich des **null** -Zeichens.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="7ff1a-119">4</span><span class="sxs-lookup"><span data-stu-id="7ff1a-119">4</span></span>

<span data-ttu-id="7ff1a-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ff1a-120">**LPWSTR**</span></span>

<span data-ttu-id="7ff1a-121">Eine auf NULL endenden Zeichenfolge mit breit Zeichen, die den Namen des Stils enthält.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="7ff1a-122">Varies</span><span class="sxs-lookup"><span data-stu-id="7ff1a-122">Varies</span></span>



 

<span data-ttu-id="7ff1a-123">Um den Stil festzulegen oder den aktuellen Stil abzurufen, verwenden Sie die [**imfsamistyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="7ff1a-124">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="7ff1a-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="7ff1a-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ff1a-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="7ff1a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ff1a-126">Requirements</span></span>



| <span data-ttu-id="7ff1a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ff1a-127">Requirement</span></span> | <span data-ttu-id="7ff1a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7ff1a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff1a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ff1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff1a-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ff1a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7ff1a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ff1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff1a-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ff1a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7ff1a-133">Header</span><span class="sxs-lookup"><span data-stu-id="7ff1a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ff1a-134"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff1a-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff1a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ff1a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff1a-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7ff1a-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ff1a-137">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="7ff1a-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7ff1a-138">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="7ff1a-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7ff1a-139">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="7ff1a-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="7ff1a-140">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="7ff1a-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ff1a-141">Sami-Medienquelle</span><span class="sxs-lookup"><span data-stu-id="7ff1a-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




