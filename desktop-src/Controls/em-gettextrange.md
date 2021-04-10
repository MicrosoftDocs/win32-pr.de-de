---
title: EM_GETTEXTRANGE Meldung (RichEdit. h)
description: Ruft einen angegebenen Zeichenbereich von einem Rich-Edit-Steuerelement ab.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Windows-Steuerelemente für EM_GETTEXTRANGE Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956901"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="4a451-104">EM \_ GetTextRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4a451-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="4a451-105">Ruft einen angegebenen Zeichenbereich von einem Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="4a451-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a451-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a451-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a451-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a451-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4a451-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a451-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a451-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a451-110">Ein Zeiger auf eine [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) -Struktur, die den Bereich der abzurufenden Zeichen und einen Puffer angibt, in den die Zeichen kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a451-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a451-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a451-111">Return value</span></span>

<span data-ttu-id="4a451-112">Die Meldung gibt die Anzahl der kopierten Zeichen zurück, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4a451-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a451-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a451-113">Requirements</span></span>



| <span data-ttu-id="4a451-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a451-114">Requirement</span></span> | <span data-ttu-id="4a451-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4a451-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a451-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a451-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a451-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a451-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a451-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a451-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a451-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a451-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a451-120">Header</span><span class="sxs-lookup"><span data-stu-id="4a451-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a451-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a451-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a451-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a451-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a451-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="4a451-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





