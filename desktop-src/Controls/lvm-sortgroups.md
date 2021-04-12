---
title: LVM_SORTGROUPS Meldung (kommstrg. h)
description: Verwendet eine Anwendungs definierte Vergleichsfunktion, um Gruppen nach ID in einem Listenansicht-Steuerelement zu sortieren.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Windows-Steuerelemente für LVM_SORTGROUPS Meldung
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105459"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="1d4fb-104">LVM \_ sortgroups-Meldung</span><span class="sxs-lookup"><span data-stu-id="1d4fb-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="1d4fb-105">Verwendet eine Anwendungs definierte Vergleichsfunktion, um Gruppen nach ID in einem Listenansicht-Steuerelement zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d4fb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d4fb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1d4fb-108">Zeiger auf eine Anwendungs definierte Vergleichsfunktion, " <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">lvgroupcompare</a>".</span><span class="sxs-lookup"><span data-stu-id="1d4fb-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="1d4fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d4fb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1d4fb-110">Void-Zeiger auf die Anwendungs definierten Informationen.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4fb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d4fb-111">Return value</span></span>

<span data-ttu-id="1d4fb-112">Gibt 1 zurück, wenn erfolgreich, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d4fb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d4fb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d4fb-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1d4fb-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d4fb-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d4fb-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d4fb-116">Requirements</span></span>



| <span data-ttu-id="1d4fb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d4fb-117">Requirement</span></span> | <span data-ttu-id="1d4fb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1d4fb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4fb-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d4fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4fb-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d4fb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d4fb-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d4fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4fb-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d4fb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d4fb-123">Header</span><span class="sxs-lookup"><span data-stu-id="1d4fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4fb-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4fb-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4fb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d4fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4fb-126">**"Lvgroupcompare"**</span><span class="sxs-lookup"><span data-stu-id="1d4fb-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

