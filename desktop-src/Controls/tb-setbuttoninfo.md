---
title: TB_SETBUTTONINFO Meldung (kommstrg. h)
description: Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Windows-Steuerelemente für TB_SETBUTTONINFO Meldung
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859239"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="1106f-104">TB \_ SetButtonInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="1106f-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="1106f-105">Legt die Informationen für eine vorhandene Schaltfläche in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="1106f-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1106f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1106f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1106f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1106f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1106f-108">Schaltflächen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1106f-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1106f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1106f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1106f-110">Ein Zeiger auf eine [**tbbuttoninfo**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) -Struktur, die die neuen Schaltflächen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="1106f-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="1106f-111">Die Member **CBSIZE** und **dwMask** dieser Struktur müssen ausgefüllt werden, bevor diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1106f-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1106f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1106f-112">Return value</span></span>

<span data-ttu-id="1106f-113">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="1106f-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1106f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1106f-114">Remarks</span></span>

<span data-ttu-id="1106f-115">Text wird normalerweise Schaltflächen zugewiesen, wenn Sie einer Symbolleiste hinzugefügt werden, indem der Index einer Zeichenfolge im Zeichen folgen Pool der Symbolleiste angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1106f-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="1106f-116">Wenn Sie eine **TB- \_ SetButtonInfo** verwenden, um einer Schaltfläche neuen Text zuzuweisen, wird der Text dauerhaft aus dem Zeichen folgen Pool überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1106f-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="1106f-117">Sie können den Text ändern, indem Sie **TB \_ SetButtonInfo** erneut aufrufen, aber Sie können die Zeichenfolge nicht aus dem Zeichen folgen Pool neu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1106f-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="1106f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1106f-118">Requirements</span></span>



| <span data-ttu-id="1106f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1106f-119">Requirement</span></span> | <span data-ttu-id="1106f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1106f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1106f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1106f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1106f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1106f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1106f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1106f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1106f-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1106f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1106f-125">Header</span><span class="sxs-lookup"><span data-stu-id="1106f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1106f-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1106f-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1106f-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="1106f-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1106f-128">**TB \_ Setbuttoninfow** (Unicode) und **TB \_ setbuttoninfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1106f-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1106f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1106f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1106f-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1106f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1106f-131">**TB ( \_ AddButtons)**</span><span class="sxs-lookup"><span data-stu-id="1106f-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="1106f-132">**TB \_ getbuttoninfo**</span><span class="sxs-lookup"><span data-stu-id="1106f-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="1106f-133">**TB \_ getbuttontext**</span><span class="sxs-lookup"><span data-stu-id="1106f-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="1106f-134">**TB \_ GetString**</span><span class="sxs-lookup"><span data-stu-id="1106f-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="1106f-135">**TB ( \_ InsertButton)**</span><span class="sxs-lookup"><span data-stu-id="1106f-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





