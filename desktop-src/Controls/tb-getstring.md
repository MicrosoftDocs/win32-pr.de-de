---
title: TB_GETSTRING Meldung (kommstrg. h)
description: Ruft eine Zeichenfolge aus dem Zeichen folgen Pool einer Symbolleiste ab.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Windows-Steuerelemente für TB_GETSTRING Meldung
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040365"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="fccb5-104">TB \_ GetString-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fccb5-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="fccb5-105">Ruft eine Zeichenfolge aus dem Zeichen folgen Pool einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="fccb5-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="fccb5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fccb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fccb5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fccb5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fccb5-108">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Länge des *LPARAM* -Puffers in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="fccb5-109">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Index der Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="fccb5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fccb5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fccb5-111">Zeiger auf einen Puffer, der zum Zurückgeben der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fccb5-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fccb5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fccb5-112">Return value</span></span>

<span data-ttu-id="fccb5-113">Gibt die Zeichen folgen Länge zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="fccb5-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fccb5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fccb5-114">Remarks</span></span>

<span data-ttu-id="fccb5-115">Diese Meldung gibt die angegebene Zeichenfolge aus dem Zeichen folgen Pool der Symbolleiste zurück.</span><span class="sxs-lookup"><span data-stu-id="fccb5-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="fccb5-116">Sie entspricht nicht notwendigerweise der Text Zeichenfolge, die derzeit von einer Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fccb5-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="fccb5-117">Um die aktuelle Text Zeichenfolge einer Schaltfläche abzurufen, senden Sie der Symbolleiste eine [**TB \_ getbuttontext**](tb-getbuttontext.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fccb5-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fccb5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fccb5-118">Requirements</span></span>



| <span data-ttu-id="fccb5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fccb5-119">Requirement</span></span> | <span data-ttu-id="fccb5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fccb5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fccb5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fccb5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fccb5-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fccb5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fccb5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fccb5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fccb5-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fccb5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fccb5-125">Header</span><span class="sxs-lookup"><span data-stu-id="fccb5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fccb5-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fccb5-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fccb5-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fccb5-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fccb5-128">**TB \_ Getstringw** (Unicode) und **TB \_ getstraninga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fccb5-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fccb5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fccb5-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="fccb5-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="fccb5-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fccb5-131">**TB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="fccb5-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="fccb5-132">**TB ( \_ AddButtons)**</span><span class="sxs-lookup"><span data-stu-id="fccb5-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="fccb5-133">**TB ( \_ InsertButton)**</span><span class="sxs-lookup"><span data-stu-id="fccb5-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

