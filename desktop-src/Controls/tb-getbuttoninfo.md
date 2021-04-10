---
title: TB_GETBUTTONINFO Meldung (kommstrg. h)
description: Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Windows-Steuerelemente für TB_GETBUTTONINFO Meldung
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106599"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="f55c8-104">TB \_ getbuttoninfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="f55c8-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="f55c8-105">Ruft erweiterte Informationen für eine Schaltfläche in einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="f55c8-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f55c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f55c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f55c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f55c8-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="f55c8-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="f55c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f55c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f55c8-110">Ein Zeiger auf eine [**tbbuttoninfo**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) -Struktur, die die Schaltflächen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f55c8-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="f55c8-111">Die Member **CBSIZE** und **dwMask** dieser Struktur müssen ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f55c8-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55c8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f55c8-112">Return value</span></span>

<span data-ttu-id="f55c8-113">Gibt den NULL basierten Index der Schaltfläche oder-1 zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="f55c8-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f55c8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f55c8-114">Remarks</span></span>

<span data-ttu-id="f55c8-115">Wenn Sie mit [**TB \_ AddButtons**](tb-addbuttons.md) oder [**TB \_ InsertButton**](tb-insertbutton.md) Schaltflächen auf der Symbolleiste platzieren, wird der Schaltflächen Text häufig durch den zugehörigen Zeichen folgen Pool Index angegeben.</span><span class="sxs-lookup"><span data-stu-id="f55c8-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="f55c8-116">**TB \_ Getbuttoninfo** ruft diese Zeichenfolge nicht ab.</span><span class="sxs-lookup"><span data-stu-id="f55c8-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="f55c8-117">Wenn Sie " **TB \_ getbuttoninfo** " zum Abrufen von Schaltflächen Text verwenden möchten, müssen Sie zunächst die Text Zeichenfolge mit " [**TB \_ SetButtonInfo**](tb-setbuttoninfo.md)" festlegen</span><span class="sxs-lookup"><span data-stu-id="f55c8-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="f55c8-118">Nachdem Sie den Schaltflächen Text mit **TB \_ SetButtonInfo** festgelegt haben, können Sie den Zeichen folgen-Pool Index nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="f55c8-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55c8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f55c8-119">Requirements</span></span>



| <span data-ttu-id="f55c8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f55c8-120">Requirement</span></span> | <span data-ttu-id="f55c8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f55c8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f55c8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f55c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f55c8-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f55c8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f55c8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f55c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f55c8-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f55c8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f55c8-126">Header</span><span class="sxs-lookup"><span data-stu-id="f55c8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55c8-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55c8-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f55c8-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f55c8-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f55c8-129">**TB \_ Getbuttoninfow** (Unicode) und **TB \_ getbuttoninfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f55c8-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f55c8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f55c8-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f55c8-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f55c8-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f55c8-132">**TB \_ SetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="f55c8-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="f55c8-133">**TB \_ getbuttontext**</span><span class="sxs-lookup"><span data-stu-id="f55c8-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





