---
title: EM_CANPASTE Meldung (RichEdit. h)
description: Bestimmt, ob ein Rich Edit-Steuerelement ein angegebenes Zwischenablage Format einfügen kann.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Windows-Steuerelemente für EM_CANPASTE Meldung
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040769"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="f08b1-104">EM \_ CanPaste-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f08b1-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="f08b1-105">Bestimmt, ob ein Rich Edit-Steuerelement ein angegebenes Zwischenablage Format einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="f08b1-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="f08b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f08b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f08b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f08b1-108">Gibt die zu Try- [Zwischenablage Formate](/windows/desktop/dataxchg/clipboard-formats) an.</span><span class="sxs-lookup"><span data-stu-id="f08b1-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="f08b1-109">Wenn Sie ein beliebiges Format in der Zwischenablage ausprobieren möchten, legen Sie diesen Parameter auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="f08b1-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f08b1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f08b1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f08b1-111">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f08b1-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08b1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f08b1-112">Return value</span></span>

<span data-ttu-id="f08b1-113">Wenn das Zwischenablage Format eingefügt werden kann, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f08b1-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="f08b1-114">Wenn das Zwischenablage Format nicht eingefügt werden kann, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f08b1-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f08b1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f08b1-115">Requirements</span></span>



| <span data-ttu-id="f08b1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f08b1-116">Requirement</span></span> | <span data-ttu-id="f08b1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f08b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f08b1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f08b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f08b1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f08b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f08b1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f08b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f08b1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f08b1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f08b1-122">Header</span><span class="sxs-lookup"><span data-stu-id="f08b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f08b1-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f08b1-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f08b1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f08b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08b1-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f08b1-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

