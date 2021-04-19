---
title: TCM_GETITEM Meldung (kommstrg. h)
description: Ruft Informationen zu einer Registerkarte in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetItem-Makros senden.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Windows-Steuerelemente für TCM_GETITEM Meldung
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343469"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="fca22-105">TCM \_ GetItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fca22-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="fca22-106">Ruft Informationen zu einer Registerkarte in einem Registerkarten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="fca22-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="fca22-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="fca22-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fca22-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fca22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fca22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fca22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fca22-110">Index der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="fca22-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="fca22-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fca22-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fca22-112">Ein Zeiger auf eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur, die die Informationen angibt, die abgerufen und Informationen über die Registerkarte empfangen werden. Wenn die Nachricht gesendet wird, gibt der **Mask** -Member an, welche Attribute zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fca22-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="fca22-113">Wenn das **Mask** -Element den tcif- \_ Textwert angibt, muss der **pszText** -Member die Adresse des Puffers enthalten, der den Element Text empfängt, und der **cchtextmax** -Member muss die Größe des Puffers angeben.</span><span class="sxs-lookup"><span data-stu-id="fca22-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fca22-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fca22-114">Return value</span></span>

<span data-ttu-id="fca22-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fca22-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fca22-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fca22-116">Remarks</span></span>

<span data-ttu-id="fca22-117">Wenn das tcif- \_ textflag im **Mask** -Member der [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur festgelegt ist, kann das Steuerelement den **pszText** -Member der Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text zu füllen.</span><span class="sxs-lookup"><span data-stu-id="fca22-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="fca22-118">Das-Steuerelement kann den **pszText** -Member auf **null** festlegen, um anzugeben, dass dem Element kein Text zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fca22-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="fca22-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fca22-119">Requirements</span></span>



| <span data-ttu-id="fca22-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fca22-120">Requirement</span></span> | <span data-ttu-id="fca22-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fca22-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fca22-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fca22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fca22-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fca22-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fca22-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fca22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fca22-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fca22-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fca22-126">Header</span><span class="sxs-lookup"><span data-stu-id="fca22-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fca22-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca22-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fca22-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fca22-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fca22-129">**TCM \_ Getitemw** (Unicode) und **TCM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fca22-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





