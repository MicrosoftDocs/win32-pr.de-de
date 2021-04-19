---
description: Gibt an, ob ein Stream geschützten Inhalt enthält.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: MF_SD_PROTECTED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362714"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="53c40-103">\_Geschütztes MF SD- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="53c40-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="53c40-104">Gibt an, ob ein Stream geschützten Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="53c40-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="53c40-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="53c40-105">Data type</span></span>

<span data-ttu-id="53c40-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="53c40-106">**UINT32**</span></span>

<span data-ttu-id="53c40-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="53c40-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c40-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53c40-108">Remarks</span></span>

<span data-ttu-id="53c40-109">Dieses Attribut gilt für streamdeskriptoren.</span><span class="sxs-lookup"><span data-stu-id="53c40-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="53c40-110">Wenn der Wert des-Attributs **true** ist, enthält der Stream geschützten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="53c40-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="53c40-111">Wenn der Wert **false** ist oder das-Attribut nicht festgelegt ist, enthält der Stream Klartext-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="53c40-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="53c40-112">Anstatt jeden Stream für dieses Attribut zu überprüfen, können Sie einen Präsentations Deskriptor an die [**mfrequireprotectedenvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="53c40-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="53c40-113">Diese Funktion testet, ob der Präsentations Deskriptor geschützte Streams enthält.</span><span class="sxs-lookup"><span data-stu-id="53c40-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="53c40-114">Eine Medienquelle sollte dieses Attribut für den Datenstrom Deskriptor festlegen, wenn der Inhalt den geschützten Medien Pfad (PMP) erfordert.</span><span class="sxs-lookup"><span data-stu-id="53c40-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="53c40-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="53c40-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="53c40-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53c40-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="53c40-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53c40-117">Requirements</span></span>



| <span data-ttu-id="53c40-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53c40-118">Requirement</span></span> | <span data-ttu-id="53c40-119">Wert</span><span class="sxs-lookup"><span data-stu-id="53c40-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53c40-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53c40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53c40-121">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="53c40-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="53c40-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53c40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53c40-123">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="53c40-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="53c40-124">Header</span><span class="sxs-lookup"><span data-stu-id="53c40-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c40-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c40-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c40-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53c40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c40-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="53c40-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="53c40-128">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="53c40-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="53c40-129">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="53c40-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="53c40-130">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="53c40-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="53c40-131">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="53c40-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




