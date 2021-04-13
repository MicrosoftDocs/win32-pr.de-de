---
title: LVM_GETGROUPSTATE Meldung (kommstrg. h)
description: Ruft den Zustand für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getgroupstate-Makros.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Windows-Steuerelemente für LVM_GETGROUPSTATE Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475375"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="3d2d4-105">LVM \_ getgroupstate-Meldung</span><span class="sxs-lookup"><span data-stu-id="3d2d4-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="3d2d4-106">Ruft den Zustand für eine angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3d2d4-106">Gets the state for a specified group.</span></span> <span data-ttu-id="3d2d4-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getgroupstate**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) -Makros.</span><span class="sxs-lookup"><span data-stu-id="3d2d4-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d2d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d2d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2d4-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2d4-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2d4-110">Gibt die Group by **igroupid** an (siehe Struktur von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ").</span><span class="sxs-lookup"><span data-stu-id="3d2d4-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="3d2d4-111">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2d4-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2d4-112">Gibt die abzurufenden Zustands Werte an.</span><span class="sxs-lookup"><span data-stu-id="3d2d4-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="3d2d4-113">Dies ist eine Kombination der Flags, die für das **State** -Mitglied von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)" aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3d2d4-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d2d4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d2d4-114">Return value</span></span>

<span data-ttu-id="3d2d4-115">Gibt die Kombination von Zustands Werten zurück, die festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3d2d4-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="3d2d4-116">Wenn z. b. *LPARAM* auf "lvgs reduziert" \_ und der zurückgegebene Wert 0 (null) ist, wird der reduzierte Status der Netzwerk Sicherheitsgruppen \_ nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="3d2d4-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="3d2d4-117">NULL wird zurückgegeben, wenn die Gruppe nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="3d2d4-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2d4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d2d4-118">Requirements</span></span>



| <span data-ttu-id="3d2d4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d2d4-119">Requirement</span></span> | <span data-ttu-id="3d2d4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3d2d4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2d4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d2d4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2d4-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d2d4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d2d4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d2d4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2d4-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d2d4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d2d4-125">Header</span><span class="sxs-lookup"><span data-stu-id="3d2d4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d2d4-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d2d4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





