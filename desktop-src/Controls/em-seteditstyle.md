---
title: EM_SETEDITSTYLE Meldung (RichEdit. h)
description: Legt die aktuellen Flags für Bearbeitungs Stile für ein Rich-Edit-Steuerelement fest.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Windows-Steuerelemente für EM_SETEDITSTYLE Meldung
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518671"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="98e5c-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="98e5c-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="98e5c-105">Legt die aktuellen Flags für Bearbeitungs Stile für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="98e5c-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="98e5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e5c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98e5c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e5c-108">Gibt ein oder mehrere Bearbeitungs Stil Flags an.</span><span class="sxs-lookup"><span data-stu-id="98e5c-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="98e5c-109">Eine Liste möglicher Werte finden Sie unter [**EM \_ GetEditStyle**](em-geteditstyle.md).</span><span class="sxs-lookup"><span data-stu-id="98e5c-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="98e5c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98e5c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e5c-111">Eine Maske, die aus einem oder mehreren der *wParam* -Werte besteht.</span><span class="sxs-lookup"><span data-stu-id="98e5c-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="98e5c-112">Nur die in dieser Maske angegebenen Werte werden festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="98e5c-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="98e5c-113">Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen flagzustände zu lesen.</span><span class="sxs-lookup"><span data-stu-id="98e5c-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e5c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98e5c-114">Return value</span></span>

<span data-ttu-id="98e5c-115">Der Rückgabewert ist der Zustand der Flags zum Bearbeiten des Stils, nachdem das Rich Edit-Steuerelement versucht hat, ihre Bearbeitungs Stiländerungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="98e5c-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="98e5c-116">Die formatierungsflags zum Bearbeiten sind ein Satz von Flags, die den aktuellen Bearbeitungs Stil angeben.</span><span class="sxs-lookup"><span data-stu-id="98e5c-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e5c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98e5c-117">Requirements</span></span>



| <span data-ttu-id="98e5c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98e5c-118">Requirement</span></span> | <span data-ttu-id="98e5c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="98e5c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98e5c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98e5c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98e5c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98e5c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98e5c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98e5c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98e5c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98e5c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98e5c-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="98e5c-124">Redistributable</span></span><br/>          | <span data-ttu-id="98e5c-125">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="98e5c-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="98e5c-126">Header</span><span class="sxs-lookup"><span data-stu-id="98e5c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e5c-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e5c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e5c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98e5c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e5c-129">**EM \_ GetEditStyle**</span><span class="sxs-lookup"><span data-stu-id="98e5c-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 





