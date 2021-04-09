---
title: LVM_ISGROUPVIEWENABLED Meldung (kommstrg. h)
description: Überprüft, ob für das Listenansicht-Steuerelement die Gruppenansicht aktiviert ist.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- Windows-Steuerelemente für LVM_ISGROUPVIEWENABLED Meldung
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956980"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="c1ca6-104">LVM- \_ isgroupviewenabled-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c1ca6-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="c1ca6-105">Überprüft, ob für das Listenansicht-Steuerelement die Gruppenansicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c1ca6-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1ca6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1ca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ca6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1ca6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c1ca6-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c1ca6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c1ca6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1ca6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c1ca6-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c1ca6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ca6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1ca6-111">Return value</span></span>

<span data-ttu-id="c1ca6-112">Gibt **true** zurück, wenn die Gruppenansicht aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c1ca6-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1ca6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1ca6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1ca6-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="c1ca6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c1ca6-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c1ca6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1ca6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1ca6-116">Requirements</span></span>



| <span data-ttu-id="c1ca6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1ca6-117">Requirement</span></span> | <span data-ttu-id="c1ca6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c1ca6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ca6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1ca6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c1ca6-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1ca6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1ca6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1ca6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c1ca6-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1ca6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1ca6-123">Header</span><span class="sxs-lookup"><span data-stu-id="c1ca6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1ca6-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1ca6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





