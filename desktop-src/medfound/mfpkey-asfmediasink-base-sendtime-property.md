---
description: Die basisend Zeit für die ASF-Medien Senke in Millisekunden.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: MFPKEY_ASFMEDIASINK_BASE_SENDTIME-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351852"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="f4401-103">Mfpkey \_ asfmediasink- \_ Basis \_ Eigenschaft sendtime</span><span class="sxs-lookup"><span data-stu-id="f4401-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="f4401-104">Die basisend Zeit für die ASF-Medien Senke in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="f4401-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="f4401-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f4401-105">Data type</span></span>

<span data-ttu-id="f4401-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="f4401-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f4401-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="f4401-107">PROPVARIANT member</span></span>

<span data-ttu-id="f4401-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="f4401-108">**ULONG**</span></span>

<span data-ttu-id="f4401-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f4401-109">VT\_UI4</span></span>

<span data-ttu-id="f4401-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="f4401-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f4401-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4401-111">Remarks</span></span>

<span data-ttu-id="f4401-112">Die Sendezeit ist die Zeit, zu der ein ASF-Paket über das Netzwerk gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4401-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="f4401-113">Sie entspricht nicht direkt der Präsentationszeit der Daten im Paket.</span><span class="sxs-lookup"><span data-stu-id="f4401-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="f4401-114">Sie können diese Eigenschaft verwenden, um die ASF-Medien Senke zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f4401-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="f4401-115">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen der ASF-Medien Senke aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="f4401-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="f4401-116">[**Mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): fragt den abgerufenen [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Zeiger für die **IPropertyStore** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="f4401-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="f4401-117">[**Mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger, der im *pcontentinfo* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f4401-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4401-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4401-118">Requirements</span></span>



| <span data-ttu-id="f4401-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4401-119">Requirement</span></span> | <span data-ttu-id="f4401-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f4401-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4401-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4401-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4401-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4401-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4401-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4401-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4401-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4401-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4401-125">Header</span><span class="sxs-lookup"><span data-stu-id="f4401-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4401-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4401-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4401-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4401-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4401-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4401-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




