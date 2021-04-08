---
title: EM_SETEDITSTYLEEX Meldung (RichEdit. h)
description: Legt die aktuellen Flags für erweiterte Bearbeitungs Stile fest.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Windows-Steuerelemente für EM_SETEDITSTYLEEX Meldung
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957003"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="a7356-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a7356-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="a7356-105">Legt die aktuellen Flags für erweiterte Bearbeitungs Stile fest.</span><span class="sxs-lookup"><span data-stu-id="a7356-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="a7356-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7356-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7356-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7356-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7356-108">Gibt ein oder mehrere erweiterte Bearbeitungs Stil-Flags an.</span><span class="sxs-lookup"><span data-stu-id="a7356-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="a7356-109">Eine Liste möglicher Werte finden Sie unter [**EM \_ geteditstyleex**](/windows/desktop/Controls/em-geteditstyleex).</span><span class="sxs-lookup"><span data-stu-id="a7356-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="a7356-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7356-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7356-111">Eine Maske, die aus einem oder mehreren der *wParam* -Werte besteht.</span><span class="sxs-lookup"><span data-stu-id="a7356-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="a7356-112">Nur die in dieser Maske angegebenen Werte werden festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a7356-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="a7356-113">Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen flagzustände zu lesen.</span><span class="sxs-lookup"><span data-stu-id="a7356-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7356-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7356-114">Return value</span></span>

<span data-ttu-id="a7356-115">Der Rückgabewert ist der Zustand der erweiterten Flags für die Bearbeitungs Formatierung, nachdem Rich Edit versucht hat, ihre Bearbeitungs Stiländerungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="a7356-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="a7356-116">Die formatierungsflags zum Bearbeiten sind ein Satz von Flags, die den aktuellen Bearbeitungs Stil angeben.</span><span class="sxs-lookup"><span data-stu-id="a7356-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7356-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7356-117">Requirements</span></span>



| <span data-ttu-id="a7356-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7356-118">Requirement</span></span> | <span data-ttu-id="a7356-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a7356-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7356-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7356-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7356-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7356-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a7356-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7356-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7356-123">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7356-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7356-124">Header</span><span class="sxs-lookup"><span data-stu-id="a7356-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7356-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7356-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7356-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7356-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7356-127">**EM \_ geteditstyleex**</span><span class="sxs-lookup"><span data-stu-id="a7356-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

