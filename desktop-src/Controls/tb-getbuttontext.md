---
title: TB_GETBUTTONTEXT Meldung (kommstrg. h)
description: Ruft den Anzeige Text einer Schaltfläche auf einer Symbolleiste ab.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Windows-Steuerelemente für TB_GETBUTTONTEXT Meldung
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104181"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="cd1d2-104">TB \_ getbuttontext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cd1d2-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="cd1d2-105">Ruft den Anzeige Text einer Schaltfläche auf einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd1d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd1d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd1d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd1d2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd1d2-108">Befehls Bezeichner der Schaltfläche, deren Text abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cd1d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd1d2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd1d2-110">Zeiger auf einen Puffer, der den Schaltflächen Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd1d2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd1d2-111">Return value</span></span>

<span data-ttu-id="cd1d2-112">Gibt die Länge der Zeichenfolge, auf die *LPARAM* zeigt, in Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="cd1d2-113">Die Länge enthält nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="cd1d2-114">Wenn nicht erfolgreich, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd1d2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd1d2-115">Remarks</span></span>

<span data-ttu-id="cd1d2-116">**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="cd1d2-117">Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="cd1d2-118">Wenn Sie diese Meldung verwenden, müssen Sie zuerst die Nachricht mit der Übergabe von **null** im *LPARAM*-Element aufzurufen. Dadurch wird die Anzahl der Zeichen zurückgegeben, ausgenommen **null** .</span><span class="sxs-lookup"><span data-stu-id="cd1d2-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="cd1d2-119">Rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="cd1d2-120">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="cd1d2-121">Die zurückgegebene Zeichenfolge entspricht dem Text, der derzeit von der Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cd1d2-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd1d2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd1d2-122">Requirements</span></span>



| <span data-ttu-id="cd1d2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd1d2-123">Requirement</span></span> | <span data-ttu-id="cd1d2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cd1d2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1d2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd1d2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd1d2-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd1d2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd1d2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd1d2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd1d2-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd1d2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd1d2-129">Header</span><span class="sxs-lookup"><span data-stu-id="cd1d2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd1d2-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd1d2-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cd1d2-131">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cd1d2-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cd1d2-132">**TB \_ Getbuttontextw** (Unicode) und **TB \_ getbuttontexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cd1d2-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="cd1d2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd1d2-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd1d2-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cd1d2-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd1d2-135">**TB \_ getbuttoninfo**</span><span class="sxs-lookup"><span data-stu-id="cd1d2-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="cd1d2-136">**TB \_ GetString**</span><span class="sxs-lookup"><span data-stu-id="cd1d2-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="cd1d2-137">**TB \_ SetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="cd1d2-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





