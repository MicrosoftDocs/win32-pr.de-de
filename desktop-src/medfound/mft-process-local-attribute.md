---
description: Gibt an, ob eine Media Foundation Transformation (MFT) nur im Anwendungsprozess registriert ist.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: MFT_PROCESS_LOCAL_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753944"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="c378e-103">\_ \_ Lokales \_ Attribut Attribut des MFT-Prozesses</span><span class="sxs-lookup"><span data-stu-id="c378e-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="c378e-104">Gibt an, ob eine Media Foundation Transformation (MFT) nur im Prozess der Anwendung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c378e-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="c378e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c378e-105">Data type</span></span>

<span data-ttu-id="c378e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c378e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c378e-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c378e-107">Get/set</span></span>

<span data-ttu-id="c378e-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c378e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c378e-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c378e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c378e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c378e-110">Remarks</span></span>

<span data-ttu-id="c378e-111">Dieses Attribut wird wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="c378e-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="c378e-112">Die Anwendung registriert eine lokale MFT, indem Sie entweder die [**mftregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) -oder die [**mftregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c378e-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="c378e-113">Diese Funktionen registrieren die MFT im Prozess der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c378e-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="c378e-114">Die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion wird aufgerufen, um MFTs aufzuzählen, die einem bestimmten Satz von Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c378e-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="c378e-115">Die Anwendung ruft die **mftenumex** -Funktion möglicherweise direkt auf, aber häufig wird diese Funktion vom topologielader aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c378e-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="c378e-116">Die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion Ruft ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern ab, die jeweils ein Aktivierungs Objekt für einen MFT darstellen.</span><span class="sxs-lookup"><span data-stu-id="c378e-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="c378e-117">Wenn eine MFT lokal registriert ist, wird das lokale Attribut Attribut des MFT- \_ Prozesses \_ \_ für das entsprechende Aktivierungs Objekt auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c378e-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="c378e-118">Der Standardwert für dieses Attribut ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c378e-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="c378e-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c378e-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c378e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c378e-120">Requirements</span></span>



| <span data-ttu-id="c378e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c378e-121">Requirement</span></span> | <span data-ttu-id="c378e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c378e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c378e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c378e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c378e-124">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c378e-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c378e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c378e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c378e-126">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c378e-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c378e-127">Header</span><span class="sxs-lookup"><span data-stu-id="c378e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c378e-128"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c378e-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c378e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c378e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c378e-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c378e-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c378e-131">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="c378e-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




