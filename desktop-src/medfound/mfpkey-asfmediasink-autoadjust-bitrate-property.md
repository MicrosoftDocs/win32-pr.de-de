---
description: Gibt an, ob die ASF-Medien Senke die Bitrate automatisch anpasst.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373423"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="bf554-103">Mfpkey \_ asfmediasink \_ autoanpassung- \_ Bitrate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf554-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="bf554-104">Gibt an, ob die ASF-Medien Senke die Bitrate automatisch anpasst.</span><span class="sxs-lookup"><span data-stu-id="bf554-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="bf554-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bf554-105">Data type</span></span>

<span data-ttu-id="bf554-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="bf554-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bf554-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="bf554-107">PROPVARIANT member</span></span>

<span data-ttu-id="bf554-108">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="bf554-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="bf554-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="bf554-109">VT\_BOOL</span></span>

<span data-ttu-id="bf554-110">**Boolesche Werte**</span><span class="sxs-lookup"><span data-stu-id="bf554-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bf554-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf554-111">Remarks</span></span>

<span data-ttu-id="bf554-112">Wenn der Wert dieser Eigenschaft Variant true ist \_ , passt die ASF-Medien Senke die Bitrate des ASF-Inhalts automatisch als Reaktion auf die Merkmale der zu multipleckenden Streams an.</span><span class="sxs-lookup"><span data-stu-id="bf554-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="bf554-113">Diese Eigenschaft wirkt sich darauf aus, wie sich die ASF-Medien Senke verhält, wenn ein Stream den "Leaky Bucket"-Parameter der Senke überschreitet</span><span class="sxs-lookup"><span data-stu-id="bf554-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="bf554-114">Wert</span><span class="sxs-lookup"><span data-stu-id="bf554-114">Value</span></span>              | <span data-ttu-id="bf554-115">Verhalten</span><span class="sxs-lookup"><span data-stu-id="bf554-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf554-116">**Variant \_ true**</span><span class="sxs-lookup"><span data-stu-id="bf554-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="bf554-117">Die ASF-Medien Senke passt die Bitrate des ASF-Inhalts automatisch als Reaktion auf die Merkmale der zu multipleckenden Streams an.</span><span class="sxs-lookup"><span data-stu-id="bf554-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="bf554-118">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="bf554-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="bf554-119">Die ASF-Medien Senke verwendet den von der Anwendung bereitgestellten Stream-Bitrate-Wert.</span><span class="sxs-lookup"><span data-stu-id="bf554-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="bf554-120">Der Standardwert ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="bf554-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="bf554-121">Legen Sie diese Eigenschaft fest, wenn Sie die ASF-Medien Senke konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bf554-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="bf554-122">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen der ASF-Medien Senke aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="bf554-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="bf554-123">[**Mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): fragt den abgerufenen [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Zeiger für die **IPropertyStore** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="bf554-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="bf554-124">[**Mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger, der im *pcontentinfo* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bf554-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="bf554-125">Wenn diese Eigenschaft auf Variant true festgelegt wird, \_ legt die ASF-Medien Senke das Flag für die **Automatische Anpassung der mfasf \_ Multiplexer- \_ \_ Bitrate** für den ASF Multiplexer fest.</span><span class="sxs-lookup"><span data-stu-id="bf554-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="bf554-126">Weitere Informationen finden Sie unter [**imfasf Multiplexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span><span class="sxs-lookup"><span data-stu-id="bf554-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="bf554-127">Weitere Informationen zum "Leaky Bucket"-Konzept finden Sie im Thema "The Leaky Bucket Buffer Model" in der Dokumentation zum Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="bf554-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf554-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf554-128">Requirements</span></span>



| <span data-ttu-id="bf554-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf554-129">Requirement</span></span> | <span data-ttu-id="bf554-130">Wert</span><span class="sxs-lookup"><span data-stu-id="bf554-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf554-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf554-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bf554-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf554-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf554-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf554-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bf554-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf554-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf554-135">Header</span><span class="sxs-lookup"><span data-stu-id="bf554-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf554-136"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf554-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf554-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf554-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf554-138">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf554-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bf554-139">**MF \_ asfstreamconfig \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="bf554-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="bf554-140">**MF \_ asfstreamconfig \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="bf554-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




