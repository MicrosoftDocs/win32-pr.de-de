---
title: EM_SETAUTOCORRECTPROC Meldung (RichEdit. h)
description: Definiert die aktuelle AutoKorrektur-Rückruf Prozedur.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Windows-Steuerelemente für EM_SETAUTOCORRECTPROC Meldung
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478591"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="ec8be-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="ec8be-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="ec8be-105">Definiert die aktuelle AutoKorrektur-Rückruf Prozedur.</span><span class="sxs-lookup"><span data-stu-id="ec8be-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="ec8be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec8be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec8be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec8be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec8be-108">Die [*autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) -Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="ec8be-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="ec8be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec8be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec8be-110">Nicht verwendet; muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ec8be-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec8be-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec8be-111">Return value</span></span>

<span data-ttu-id="ec8be-112">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ec8be-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="ec8be-113">Wenn der Vorgang fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ec8be-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec8be-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec8be-114">Requirements</span></span>



| <span data-ttu-id="ec8be-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec8be-115">Requirement</span></span> | <span data-ttu-id="ec8be-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ec8be-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8be-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec8be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8be-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec8be-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ec8be-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec8be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8be-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec8be-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec8be-121">Header</span><span class="sxs-lookup"><span data-stu-id="ec8be-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec8be-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec8be-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec8be-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec8be-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8be-124">*Autocorrectproc*</span><span class="sxs-lookup"><span data-stu-id="ec8be-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="ec8be-125">**EM \_ callautocorrectproc**</span><span class="sxs-lookup"><span data-stu-id="ec8be-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="ec8be-126">**EM \_ getautocorrectproc**</span><span class="sxs-lookup"><span data-stu-id="ec8be-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





