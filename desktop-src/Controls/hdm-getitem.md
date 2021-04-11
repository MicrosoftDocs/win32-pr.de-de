---
title: HDM_GETITEM Meldung (kommstrg. h)
description: Ruft Informationen zu einem Element in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ GetItem-Makro verwenden.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- Windows-Steuerelemente für HDM_GETITEM Meldung
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103778"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="4d9eb-105">HDM- \_ GetItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4d9eb-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="4d9eb-106">Ruft Informationen zu einem Element in einem Header Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="4d9eb-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d9eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d9eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d9eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d9eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d9eb-110">Der Index des Elements, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="4d9eb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d9eb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d9eb-112">Ein Zeiger auf eine [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="4d9eb-113">Wenn die Nachricht gesendet wird, gibt das **Masken** Element den Typ der angeforderten Informationen an.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="4d9eb-114">Wenn die Meldung zurückgegeben wird, erhalten die anderen Member die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="4d9eb-115">Wenn das **Masken** Element NULL angibt, gibt die Meldung **true** zurück, kopiert jedoch keine Informationen in die Struktur.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d9eb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d9eb-116">Return value</span></span>

<span data-ttu-id="4d9eb-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4d9eb-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d9eb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d9eb-118">Remarks</span></span>

<span data-ttu-id="4d9eb-119">Wenn das HDI- \_ textflag im **Mask** -Member der [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur festgelegt ist, kann das Steuerelement den **pszText** -Member der Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text zu füllen.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="4d9eb-120">Anwendungen sollten nicht davon ausgehen, dass der Text immer in den angeforderten Puffer eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4d9eb-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d9eb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d9eb-121">Requirements</span></span>



| <span data-ttu-id="4d9eb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d9eb-122">Requirement</span></span> | <span data-ttu-id="4d9eb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4d9eb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9eb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d9eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d9eb-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d9eb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d9eb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d9eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d9eb-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d9eb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d9eb-128">Header</span><span class="sxs-lookup"><span data-stu-id="4d9eb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d9eb-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d9eb-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4d9eb-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="4d9eb-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4d9eb-131">**HDM \_ Getitemw** (Unicode) und **HDM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4d9eb-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





