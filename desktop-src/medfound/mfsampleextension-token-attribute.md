---
description: 'Enthält einen Zeiger auf das Token, das für die imfmediastream:: requestsample-Methode bereitgestellt wurde.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: MFSampleExtension_Token-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350530"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="2ee12-103">MF Sample Extension- \_ tokenattribut</span><span class="sxs-lookup"><span data-stu-id="2ee12-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="2ee12-104">Enthält einen Zeiger auf das Token, das für die [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ee12-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ee12-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2ee12-105">Data type</span></span>

<span data-ttu-id="2ee12-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="2ee12-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="2ee12-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="2ee12-107">Get/set</span></span>

<span data-ttu-id="2ee12-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="2ee12-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="2ee12-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="2ee12-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2ee12-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="2ee12-110">Applies to</span></span>

[<span data-ttu-id="2ee12-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="2ee12-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="2ee12-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ee12-112">Remarks</span></span>

<span data-ttu-id="2ee12-113">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="2ee12-113">This attribute applies to media samples.</span></span> <span data-ttu-id="2ee12-114">Der Wert des-Attributs ist der **IUnknown** -Zeiger, der an den *pToken* -Parameter der [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ee12-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="2ee12-115">Der Aufrufer verwendet dieses Attribut, um den Status der Anforderung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2ee12-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="2ee12-116">Wenn Sie eine benutzerdefinierte Medienquelle schreiben, legen Sie dieses Attribut für das Beispiel fest, wenn der Mediendaten Strom ein Beispiel als Antwort auf die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode liefert, es sei denn, der Wert von *pToken* ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2ee12-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="2ee12-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="2ee12-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee12-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ee12-118">Requirements</span></span>



| <span data-ttu-id="2ee12-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ee12-119">Requirement</span></span> | <span data-ttu-id="2ee12-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2ee12-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee12-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ee12-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee12-122">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2ee12-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2ee12-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ee12-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee12-124">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2ee12-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2ee12-125">Header</span><span class="sxs-lookup"><span data-stu-id="2ee12-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee12-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee12-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee12-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ee12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee12-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2ee12-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ee12-129">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="2ee12-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ee12-130">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ee12-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




