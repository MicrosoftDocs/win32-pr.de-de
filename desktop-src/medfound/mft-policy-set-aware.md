---
description: Gibt an, ob imftransform MEPolicySet-Abschluss Benachrichtigungen empfangen möchte.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345264"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="a2439-103">MFT- \_ Richtlinien \_ Satz fähiges \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="a2439-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="a2439-104">Wenn ungleich 0 (null), gibt an, dass die **imftransform** -Meldung über das Beenden von [MEPolicySet](./mepolicyset.md) -Benachrichtigungen empfangen möchte</span><span class="sxs-lookup"><span data-stu-id="a2439-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2439-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2439-105">Data type</span></span>

<span data-ttu-id="a2439-106">**UInt32** (als **bool** behandelt)</span><span class="sxs-lookup"><span data-stu-id="a2439-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="a2439-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="a2439-107">Get/set</span></span>

<span data-ttu-id="a2439-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a2439-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a2439-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a2439-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a2439-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="a2439-110">Applies to</span></span>

[<span data-ttu-id="a2439-111">**Imfinputtrustauthority**</span><span class="sxs-lookup"><span data-stu-id="a2439-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="a2439-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2439-112">Remarks</span></span>

<span data-ttu-id="a2439-113">Dieses attributetett kann von einer **imfinputtrustauthority** -Entschlüsselung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2439-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="a2439-114">Eine Implementierung eines Inhalts Entschlüsselungs Moduls (CDM) kann eine Implementierung von **imfinputtrustauthority** enthalten.</span><span class="sxs-lookup"><span data-stu-id="a2439-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="a2439-115">Der Zugriff auf das **imfinputtrustauthority** -Objekt erfolgt über [IMF contentdecryptionmodule:: foratetrustedinput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span><span class="sxs-lookup"><span data-stu-id="a2439-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="a2439-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a2439-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2439-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2439-117">Requirements</span></span>



| <span data-ttu-id="a2439-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2439-118">Requirement</span></span> | <span data-ttu-id="a2439-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a2439-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2439-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2439-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2439-121">Windows 10 April 2020-Update</span><span class="sxs-lookup"><span data-stu-id="a2439-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="a2439-122">Header</span><span class="sxs-lookup"><span data-stu-id="a2439-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2439-123"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a2439-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2439-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2439-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2439-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a2439-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="a2439-126">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="a2439-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
