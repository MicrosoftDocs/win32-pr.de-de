---
title: LVM_GETFOCUSEDGROUP Meldung (kommstrg. h)
description: Ruft die Gruppe ab, die den Fokus besitzt. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfocusedgroup-Makros.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Windows-Steuerelemente für LVM_GETFOCUSEDGROUP Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475165"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="25d92-105">LVM \_ getfocusedgroup-Meldung</span><span class="sxs-lookup"><span data-stu-id="25d92-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="25d92-106">Ruft die Gruppe ab, die den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="25d92-106">Gets the group that has the focus.</span></span> <span data-ttu-id="25d92-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfocusedgroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) -Makros.</span><span class="sxs-lookup"><span data-stu-id="25d92-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25d92-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="25d92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25d92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25d92-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25d92-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="25d92-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25d92-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25d92-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="25d92-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="25d92-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25d92-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25d92-113">Return value</span></span>

<span data-ttu-id="25d92-114">Gibt den Index der Gruppe mit dem Status "mit \_ Fokus" oder "-1" zurück, wenn keine Gruppe mit dem Status "lvgs" fokussiert ist \_ .</span><span class="sxs-lookup"><span data-stu-id="25d92-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="25d92-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25d92-115">Requirements</span></span>



| <span data-ttu-id="25d92-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25d92-116">Requirement</span></span> | <span data-ttu-id="25d92-117">Wert</span><span class="sxs-lookup"><span data-stu-id="25d92-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25d92-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25d92-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25d92-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25d92-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25d92-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25d92-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25d92-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25d92-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25d92-122">Header</span><span class="sxs-lookup"><span data-stu-id="25d92-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25d92-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="25d92-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





