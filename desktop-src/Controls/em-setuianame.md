---
title: EM_SETUIANAME Meldung (RichEdit. h)
description: Legt den Namen eines Rich-Edit-Steuer Elements für die Benutzeroberflächen Automatisierung (UIA) fest.
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Windows-Steuerelemente für EM_SETUIANAME Meldung
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956634"
---
# <a name="em_setuianame-message"></a><span data-ttu-id="6b8d4-104">EM \* \_ tuianame-Meldung</span><span class="sxs-lookup"><span data-stu-id="6b8d4-104">EM\_SETUIANAME message</span></span>

<span data-ttu-id="6b8d4-105">Legt den Namen eines Rich-Edit-Steuer Elements für die Benutzeroberflächen Automatisierung (UIA) fest.</span><span class="sxs-lookup"><span data-stu-id="6b8d4-105">Sets the name of a rich edit control for UI Automation (UIA).</span></span>


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a><span data-ttu-id="6b8d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b8d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b8d4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8d4-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6b8d4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b8d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b8d4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8d4-110">Ein Zeiger auf die NULL-terminierte namens Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b8d4-110">A pointer to the null-terminated name string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8d4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b8d4-111">Return value</span></span>

<span data-ttu-id="6b8d4-112">TRUE, wenn der Name für die UIA erfolgreich festgelegt wurde, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="6b8d4-112">TRUE if the name for UIA is successfully set, otherwise FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8d4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b8d4-113">Requirements</span></span>



| <span data-ttu-id="6b8d4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b8d4-114">Requirement</span></span> | <span data-ttu-id="6b8d4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6b8d4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8d4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b8d4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8d4-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b8d4-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b8d4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b8d4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8d4-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b8d4-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b8d4-120">Header</span><span class="sxs-lookup"><span data-stu-id="6b8d4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b8d4-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8d4-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





