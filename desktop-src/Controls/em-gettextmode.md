---
title: EM_GETTEXTMODE Meldung (RichEdit. h)
description: Ruft den aktuellen Textmodus und die rückgängig-Ebene eines Rich-Edit-Steuer Elements ab.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Windows-Steuerelemente für EM_GETTEXTMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478114"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="e2c28-104">EM \_ gettextmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="e2c28-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="e2c28-105">Ruft den aktuellen Textmodus und die rückgängig-Ebene eines Rich-Edit-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="e2c28-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2c28-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2c28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2c28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2c28-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e2c28-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2c28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2c28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2c28-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e2c28-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c28-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2c28-111">Return value</span></span>

<span data-ttu-id="e2c28-112">Der Rückgabewert ist ein oder mehrere Werte aus dem [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="e2c28-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="e2c28-113">Die Werte geben den aktuellen Textmodus und die rückgängig-Ebene des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="e2c28-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c28-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2c28-114">Requirements</span></span>



| <span data-ttu-id="e2c28-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2c28-115">Requirement</span></span> | <span data-ttu-id="e2c28-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e2c28-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c28-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2c28-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c28-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2c28-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2c28-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2c28-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c28-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2c28-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2c28-121">Header</span><span class="sxs-lookup"><span data-stu-id="e2c28-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c28-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c28-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c28-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2c28-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2c28-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e2c28-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2c28-125">**EM \_ settextmode**</span><span class="sxs-lookup"><span data-stu-id="e2c28-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="e2c28-126">**TextMode**</span><span class="sxs-lookup"><span data-stu-id="e2c28-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





