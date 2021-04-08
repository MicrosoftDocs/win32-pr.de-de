---
description: Gibt an, wie die ASF-Medien Senke Windows Media DRM anwenden soll.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761478"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="40f32-103">Mfpkey \_ asfmediasink \_ drmaction (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40f32-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="40f32-104">Gibt an, wie die ASF-Medien Senke Windows Media DRM anwenden soll.</span><span class="sxs-lookup"><span data-stu-id="40f32-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="40f32-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="40f32-105">Data type</span></span>

<span data-ttu-id="40f32-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="40f32-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="40f32-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="40f32-107">PROPVARIANT member</span></span>

<span data-ttu-id="40f32-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="40f32-108">**ULONG**</span></span>

<span data-ttu-id="40f32-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="40f32-109">VT\_UI4</span></span>

<span data-ttu-id="40f32-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="40f32-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="40f32-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40f32-111">Remarks</span></span>

<span data-ttu-id="40f32-112">Der Wert dieser Eigenschaft ist ein Member der [**mfsink \_ wmdrmaction**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="40f32-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="40f32-113">Sie können dieses Attribut verwenden, um die ASF-Medien Senke zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="40f32-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="40f32-114">Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen der ASF-Medien Senke aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="40f32-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="40f32-115">[**Mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): fragt den abgerufenen [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Zeiger für die **IPropertyStore** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="40f32-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="40f32-116">[**Mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger, der im *pcontentinfo* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="40f32-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f32-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40f32-117">Requirements</span></span>



| <span data-ttu-id="40f32-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40f32-118">Requirement</span></span> | <span data-ttu-id="40f32-119">Wert</span><span class="sxs-lookup"><span data-stu-id="40f32-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40f32-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40f32-120">Minimum supported client</span></span><br/> | <span data-ttu-id="40f32-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40f32-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="40f32-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40f32-122">Minimum supported server</span></span><br/> | <span data-ttu-id="40f32-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40f32-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="40f32-124">Header</span><span class="sxs-lookup"><span data-stu-id="40f32-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f32-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f32-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f32-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40f32-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f32-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40f32-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
