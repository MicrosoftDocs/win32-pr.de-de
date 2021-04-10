---
title: CB_INITSTORAGE Meldung (Winuser. h)
description: Eine Anwendung sendet die CB \_ InitStorage-Nachricht, bevor eine große Anzahl von Elementen zum Listenfeld Teil eines Kombinations Felds hinzugefügt wird. Diese Meldung weist Speicher zum Speichern von Listenfeld Elementen zu.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- Windows-Steuerelemente für CB_INITSTORAGE Meldung
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103627"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="9f2b1-105">CB- \_ InitStorage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9f2b1-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="9f2b1-106">Eine Anwendung sendet die **CB \_ InitStorage** -Nachricht, bevor eine große Anzahl von Elementen zum Listenfeld Teil eines Kombinations Felds hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="9f2b1-107">Diese Meldung weist Speicher zum Speichern von Listenfeld Elementen zu.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f2b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f2b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2b1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f2b1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f2b1-110">Die Anzahl der hinzu zufügenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="9f2b1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f2b1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f2b1-112">Die Menge an Arbeitsspeicher, die für Element Zeichenfolgen in Bytes belegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2b1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f2b1-113">Return value</span></span>

<span data-ttu-id="9f2b1-114">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Elemente, für die Speicher reserviert wurde, d. h. die Gesamtanzahl der Elemente, die von allen erfolgreichen **CB- \_ InitStorage** -Nachrichten hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="9f2b1-115">Wenn die Meldung fehlschlägt, ist der Rückgabewert CB \_ errspace.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="9f2b1-116">Die Meldung weist Arbeitsspeicher zu und gibt die oben beschriebenen Erfolgs-und Fehler Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f2b1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f2b1-117">Remarks</span></span>

<span data-ttu-id="9f2b1-118">Die **CB \_ InitStorage** -Nachricht beschleunigt die Initialisierung von Kombinations Feldern, die über eine große Anzahl von Elementen (über 100) verfügen.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="9f2b1-119">Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende [**CB \_ AddString**](cb-addstring.md)-, [**CB \_ InsertString**](cb-insertstring.md)-und [**CB- \_ dir**](cb-dir.md) -Nachrichten die kürzeste Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="9f2b1-120">Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="9f2b1-121">Wenn Sie die Schätzung überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie dies unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2b1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f2b1-122">Requirements</span></span>



| <span data-ttu-id="9f2b1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f2b1-123">Requirement</span></span> | <span data-ttu-id="9f2b1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9f2b1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2b1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f2b1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2b1-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f2b1-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f2b1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f2b1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2b1-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f2b1-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f2b1-129">Header</span><span class="sxs-lookup"><span data-stu-id="9f2b1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f2b1-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9f2b1-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2b1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f2b1-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f2b1-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9f2b1-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f2b1-133">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="9f2b1-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="9f2b1-134">**CB- \_ dir**</span><span class="sxs-lookup"><span data-stu-id="9f2b1-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="9f2b1-135">**CB \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="9f2b1-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





