---
title: LVM_GETFOOTERITEM Meldung (kommstrg. h)
description: Ruft Informationen zu einem footerelement in einem Listenansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooteritem-Makros.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERITEM Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040100"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="5c931-105">LVM- \_ getfooteritem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5c931-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="5c931-106">Ruft Informationen zu einem footerelement in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="5c931-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="5c931-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooteritem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) -Makros.</span><span class="sxs-lookup"><span data-stu-id="5c931-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c931-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c931-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c931-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c931-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c931-110">Der Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="5c931-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="5c931-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5c931-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c931-112">Ein Zeiger auf eine " [**lvfooteritem**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) "-Struktur, die einen Wert für den **Zustand** und/oder **pszText** -Member gemäß dem Wert des **Masken** Members empfängt.</span><span class="sxs-lookup"><span data-stu-id="5c931-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="5c931-113">Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und deren Member festzulegen, um dem Empfänger anzugeben, welche Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c931-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="5c931-114">Weitere Informationen finden Sie unter " **lvfooteritem**".</span><span class="sxs-lookup"><span data-stu-id="5c931-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c931-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c931-115">Return value</span></span>

<span data-ttu-id="5c931-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5c931-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c931-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c931-117">Requirements</span></span>



| <span data-ttu-id="5c931-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c931-118">Requirement</span></span> | <span data-ttu-id="5c931-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5c931-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c931-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c931-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5c931-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c931-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c931-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c931-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5c931-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c931-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c931-124">Header</span><span class="sxs-lookup"><span data-stu-id="5c931-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c931-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c931-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





