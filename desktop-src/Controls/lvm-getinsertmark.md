---
title: LVM_GETINSERTMARK Meldung (kommstrg. h)
description: Ruft die Position der Einfügemarke ab.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Windows-Steuerelemente für LVM_GETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858784"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="8c766-104">LVM \_ getinsertmark-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8c766-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="8c766-105">Ruft die Position der Einfügemarke ab.</span><span class="sxs-lookup"><span data-stu-id="8c766-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c766-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c766-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c766-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c766-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8c766-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8c766-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8c766-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c766-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8c766-110">Ein Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">lvinsertmark</a> -Struktur, die die Position der Einfügemarke empfängt.</span><span class="sxs-lookup"><span data-stu-id="8c766-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c766-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c766-111">Return value</span></span>

<span data-ttu-id="8c766-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8c766-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="8c766-113">**False** wird zurückgegeben, wenn die Größe im **CBSIZE** -Member der [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur nicht der tatsächlichen Größe der Struktur entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c766-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c766-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c766-114">Remarks</span></span>

<span data-ttu-id="8c766-115">Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansicht-Steuerelement in der Symbol Ansicht, in der kleinen Symbol Ansicht oder in der Kachel Ansicht befindet und sich nicht im gruppenansichts Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="8c766-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="8c766-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="8c766-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8c766-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c766-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c766-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c766-118">Requirements</span></span>



| <span data-ttu-id="8c766-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c766-119">Requirement</span></span> | <span data-ttu-id="8c766-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8c766-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c766-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c766-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c766-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c766-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c766-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c766-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c766-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c766-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c766-125">Header</span><span class="sxs-lookup"><span data-stu-id="8c766-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c766-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c766-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





