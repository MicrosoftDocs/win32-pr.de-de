---
title: EM_GETAUTOCORRECTPROC Meldung (RichEdit. h)
description: Ruft einen Zeiger auf die Anwendungs definierte autocorrectproc-Funktion ab.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Windows-Steuerelemente für EM_GETAUTOCORRECTPROC Meldung
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477115"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="d1213-104">EM \_ getautocorrectproc-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d1213-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="d1213-105">Ruft einen Zeiger auf die Anwendungs definierte [*autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) -Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="d1213-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1213-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1213-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1213-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1213-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1213-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d1213-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d1213-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1213-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1213-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d1213-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1213-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1213-111">Return value</span></span>

<span data-ttu-id="d1213-112">Gibt einen Zeiger auf die Anwendungs definierte [*autocorrectproc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="d1213-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1213-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1213-113">Requirements</span></span>



| <span data-ttu-id="d1213-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1213-114">Requirement</span></span> | <span data-ttu-id="d1213-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d1213-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1213-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1213-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1213-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1213-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d1213-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1213-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1213-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1213-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1213-120">Header</span><span class="sxs-lookup"><span data-stu-id="d1213-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1213-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1213-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1213-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1213-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1213-123">*Autocorrectproc*</span><span class="sxs-lookup"><span data-stu-id="d1213-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="d1213-124">**EM \_ callautocorrectproc**</span><span class="sxs-lookup"><span data-stu-id="d1213-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="d1213-125">**EM- \_ tautkorrigitproc**</span><span class="sxs-lookup"><span data-stu-id="d1213-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





