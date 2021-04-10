---
title: CB_GETTOPINDEX Meldung (Winuser. h)
description: Eine Anwendung sendet die CB \_ gettopindex-Nachricht, um den NULL basierten Index des ersten sichtbaren Elements im Listenfeld Teil eines Kombinations Felds abzurufen.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Windows-Steuerelemente für CB_GETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956452"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="728c9-104">CB \_ gettopindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="728c9-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="728c9-105">Eine Anwendung sendet die **CB \_ gettopindex** -Nachricht, um den NULL basierten Index des ersten sichtbaren Elements im Listenfeld Teil eines Kombinations Felds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="728c9-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="728c9-106">Anfänglich befindet sich das Element mit dem Index 0 am oberen Rand des Listen Felds, aber wenn für den Listenfeld Inhalt ein Bildlauf ausgeführt wurde, befindet sich möglicherweise ein anderes Element im oberen Bereich.</span><span class="sxs-lookup"><span data-stu-id="728c9-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="728c9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="728c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="728c9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="728c9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="728c9-109">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="728c9-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="728c9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="728c9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="728c9-111">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="728c9-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="728c9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="728c9-112">Return value</span></span>

<span data-ttu-id="728c9-113">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der Index des ersten sichtbaren Elements im Listenfeld des Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="728c9-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="728c9-114">Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="728c9-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="728c9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="728c9-115">Requirements</span></span>



| <span data-ttu-id="728c9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="728c9-116">Requirement</span></span> | <span data-ttu-id="728c9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="728c9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="728c9-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="728c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="728c9-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="728c9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="728c9-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="728c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="728c9-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="728c9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="728c9-122">Header</span><span class="sxs-lookup"><span data-stu-id="728c9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="728c9-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="728c9-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="728c9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="728c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728c9-125">**CB \_ settopindex**</span><span class="sxs-lookup"><span data-stu-id="728c9-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 





