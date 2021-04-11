---
title: Inapcomponentinfo-Schnittstelle (napcommon. h)
description: Stellt Methoden bereit, die von Plug-in-Komponenten (z. b. SHAs und SHVs) implementiert werden müssen, damit das NAP-System mit Ihnen kommuniziert.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- Inapcomponentinfo-Schnittstelle NAP
- Inapcomponentinfo-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949670"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="6a07b-105">Inapcomponentinfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6a07b-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="6a07b-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a07b-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6a07b-107">Die **inapcomponentinfo** -Schnittstelle stellt Methoden bereit, die von Plug-in-Komponenten (z. b. SHAs und SHVs) implementiert werden müssen, damit das NAP-System mit Ihnen kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="6a07b-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="6a07b-108">Das NAP-System ruft Ihre Implementierung dieser Methoden auf, um statische administrative Informationen (z. b. Anzeige Name oder lokalisierte Zeichen folgen) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a07b-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="6a07b-109">Member</span><span class="sxs-lookup"><span data-stu-id="6a07b-109">Members</span></span>

<span data-ttu-id="6a07b-110">Die **inapcomponentinfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6a07b-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6a07b-111">**Inapcomponentinfo** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6a07b-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="6a07b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a07b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a07b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a07b-113">Methods</span></span>

<span data-ttu-id="6a07b-114">Die **inapcomponentinfo** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6a07b-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="6a07b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="6a07b-115">Method</span></span>                                                                                                         | <span data-ttu-id="6a07b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a07b-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a07b-117">**Inapcomponentinfo:: converterrorcodetomess ageid**</span><span class="sxs-lookup"><span data-stu-id="6a07b-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="6a07b-118">Wird vom NAP-System verwendet, um anzufordern, dass der Integritäts Client einen HRESULT-Fehlercode in eine Nachrichten-ID konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6a07b-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="6a07b-119">**Inapcomponentinfo:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="6a07b-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="6a07b-120">Wird vom NAP-System verwendet, um die Beschreibung eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a07b-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="6a07b-121">**Inapcomponentinfo:: getfriendlyname**</span><span class="sxs-lookup"><span data-stu-id="6a07b-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="6a07b-122">Wird vom NAP-System verwendet, um den anzeigen Amen eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a07b-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="6a07b-123">**Inapcomponentinfo:: getIcon**</span><span class="sxs-lookup"><span data-stu-id="6a07b-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="6a07b-124">Wird vom NAP-System verwendet, um das Symbol eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a07b-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="6a07b-125">**Inapcomponentinfo:: GetLocalizedString**</span><span class="sxs-lookup"><span data-stu-id="6a07b-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="6a07b-126">Wird vom NAP-System verwendet, um lokalisierte Zeichen folgen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a07b-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="6a07b-127">**Inapcomponentinfo:: getvendorname**</span><span class="sxs-lookup"><span data-stu-id="6a07b-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="6a07b-128">Wird vom NAP-System verwendet, um den Herstellernamen eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a07b-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="6a07b-129">**Inapcomponentinfo:: GetVersion**</span><span class="sxs-lookup"><span data-stu-id="6a07b-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="6a07b-130">Wird vom NAP-System verwendet, um die Version eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a07b-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="6a07b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a07b-131">Requirements</span></span>



| <span data-ttu-id="6a07b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a07b-132">Requirement</span></span> | <span data-ttu-id="6a07b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6a07b-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a07b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a07b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6a07b-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a07b-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6a07b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a07b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6a07b-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a07b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a07b-138">Header</span><span class="sxs-lookup"><span data-stu-id="6a07b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a07b-139"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a07b-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a07b-140">IDL</span><span class="sxs-lookup"><span data-stu-id="6a07b-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a07b-141"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a07b-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a07b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a07b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a07b-143">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6a07b-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6a07b-144">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="6a07b-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

