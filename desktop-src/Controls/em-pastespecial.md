---
title: EM_PASTESPECIAL Meldung (RichEdit. h)
description: Fügt ein bestimmtes Zwischenablage Format in einem Rich-Edit-Steuerelement ein.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Windows-Steuerelemente für EM_PASTESPECIAL Meldung
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859016"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="b773a-104">\_Gepastespecial Nachricht</span><span class="sxs-lookup"><span data-stu-id="b773a-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="b773a-105">Fügt ein bestimmtes Zwischenablage Format in einem Rich-Edit-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="b773a-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b773a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b773a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b773a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b773a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b773a-108">Gibt die [Zwischenablage Formate](/windows/desktop/dataxchg/clipboard-formats)an.</span><span class="sxs-lookup"><span data-stu-id="b773a-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="b773a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b773a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b773a-110">Zeiger auf eine [**repastespecial**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) -Struktur oder **null**.</span><span class="sxs-lookup"><span data-stu-id="b773a-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="b773a-111">Wenn ein Objekt eingefügt wird, wird die **repastespecial** -Struktur mit dem gewünschten Anzeige Aspekt ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b773a-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="b773a-112">Wenn *LPARAM* **null** ist oder der **dwAspect** -Member 0 (null) ist, ist der verwendete Anzeige Aspekt der Inhalt des Objekt Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="b773a-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b773a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b773a-113">Return value</span></span>

<span data-ttu-id="b773a-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b773a-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b773a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b773a-115">Requirements</span></span>



| <span data-ttu-id="b773a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b773a-116">Requirement</span></span> | <span data-ttu-id="b773a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b773a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b773a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b773a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b773a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b773a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b773a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b773a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b773a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b773a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b773a-122">Header</span><span class="sxs-lookup"><span data-stu-id="b773a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b773a-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b773a-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b773a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b773a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b773a-125">**Repastespecial**</span><span class="sxs-lookup"><span data-stu-id="b773a-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

