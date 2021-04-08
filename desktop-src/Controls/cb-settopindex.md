---
title: CB_SETTOPINDEX Meldung (Winuser. h)
description: Eine Anwendung sendet die CB- \_ settopindex-Nachricht, um sicherzustellen, dass ein bestimmtes Element im Listenfeld eines Kombinations Felds sichtbar ist.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Windows-Steuerelemente für CB_SETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740120"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="39c21-104">CB \_ settopindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="39c21-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="39c21-105">Eine Anwendung sendet die **CB- \_ settopindex** -Nachricht, um sicherzustellen, dass ein bestimmtes Element im Listenfeld eines Kombinations Felds sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="39c21-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="39c21-106">Das System führt einen Bildlauf im Listenfeld Inhalt durch, sodass entweder das angegebene Element oben im Listenfeld angezeigt wird oder der maximale Bild Laufbereich erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="39c21-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="39c21-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="39c21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c21-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39c21-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39c21-109">Gibt den NULL basierten Index des Listen Elements an.</span><span class="sxs-lookup"><span data-stu-id="39c21-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="39c21-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39c21-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39c21-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c21-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c21-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39c21-112">Return value</span></span>

<span data-ttu-id="39c21-113">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="39c21-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="39c21-114">Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="39c21-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c21-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39c21-115">Requirements</span></span>



| <span data-ttu-id="39c21-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39c21-116">Requirement</span></span> | <span data-ttu-id="39c21-117">Wert</span><span class="sxs-lookup"><span data-stu-id="39c21-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c21-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39c21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39c21-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39c21-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39c21-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39c21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39c21-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39c21-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39c21-122">Header</span><span class="sxs-lookup"><span data-stu-id="39c21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c21-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="39c21-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c21-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39c21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c21-125">**CB \_ gettopindex**</span><span class="sxs-lookup"><span data-stu-id="39c21-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 





