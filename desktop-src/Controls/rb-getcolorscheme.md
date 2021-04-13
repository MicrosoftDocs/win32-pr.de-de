---
title: RB_GETCOLORSCHEME Meldung (kommstrg. h)
description: Ruft die Farbschema Informationen aus dem Grund leisten-Steuerelement ab.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- Windows-Steuerelemente für RB_GETCOLORSCHEME Meldung
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518278"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="55eec-104">RB \_ getcolorscheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="55eec-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="55eec-105">Ruft die Farbschema Informationen aus dem Grund leisten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="55eec-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="55eec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55eec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55eec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55eec-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="55eec-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="55eec-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="55eec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55eec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55eec-110">Zeiger auf eine [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) -Struktur, die die Farbschema Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="55eec-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="55eec-111">Sie müssen den **dwSize** -Member dieser Struktur auf **sizeof**(ColorScheme) festlegen, bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="55eec-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55eec-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55eec-112">Return value</span></span>

<span data-ttu-id="55eec-113">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="55eec-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="55eec-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55eec-114">Requirements</span></span>



| <span data-ttu-id="55eec-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55eec-115">Requirement</span></span> | <span data-ttu-id="55eec-116">Wert</span><span class="sxs-lookup"><span data-stu-id="55eec-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55eec-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55eec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55eec-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55eec-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55eec-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55eec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55eec-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55eec-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55eec-121">Header</span><span class="sxs-lookup"><span data-stu-id="55eec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="55eec-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="55eec-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55eec-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55eec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55eec-124">**RB \_ SetColorScheme**</span><span class="sxs-lookup"><span data-stu-id="55eec-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





