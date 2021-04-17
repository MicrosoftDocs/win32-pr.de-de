---
title: LB_INITSTORAGE Meldung (Winuser. h)
description: Ordnet Arbeitsspeicher zum Speichern von Listenfeld Elementen zu. Diese Meldung wird verwendet, bevor eine Anwendung eine große Anzahl von Elementen zu einem Listenfeld hinzufügt.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Windows-Steuerelemente für LB_INITSTORAGE Meldung
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476815"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="1f870-105">LB- \_ InitStorage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1f870-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="1f870-106">Ordnet Arbeitsspeicher zum Speichern von Listenfeld Elementen zu.</span><span class="sxs-lookup"><span data-stu-id="1f870-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="1f870-107">Diese Meldung wird verwendet, bevor eine Anwendung eine große Anzahl von Elementen zu einem Listenfeld hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="1f870-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f870-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f870-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f870-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f870-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f870-110">Die Anzahl der hinzu zufügenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="1f870-110">The number of items to add.</span></span>

<span data-ttu-id="1f870-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1f870-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="1f870-112">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="1f870-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="1f870-113">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1f870-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="1f870-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f870-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f870-115">Die Größe des Arbeitsspeichers in Bytes, der für Element Zeichenfolgen belegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f870-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f870-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f870-116">Return value</span></span>

<span data-ttu-id="1f870-117">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Elemente, für die Speicher reserviert wurde, d. h. die Gesamtanzahl der Elemente, die von allen erfolgreichen **lb- \_ InitStorage** -Nachrichten hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="1f870-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="1f870-118">Wenn die Meldung fehlschlägt, ist der Rückgabewert "lb \_ errspace".</span><span class="sxs-lookup"><span data-stu-id="1f870-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="1f870-119">Microsoft Windows NT 4,0: Diese Nachricht weist nicht die angegebene Arbeitsspeicher Menge zu. Allerdings wird immer der im *wParam* -Parameter angegebene Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f870-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f870-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f870-120">Remarks</span></span>

<span data-ttu-id="1f870-121">Die " **lb- \_ InitStorage** "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen.</span><span class="sxs-lookup"><span data-stu-id="1f870-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="1f870-122">Sie reserviert die angegebene Arbeitsspeicher Menge, sodass nachfolgende [**lb- \_ AddString**](lb-addstring.md)-, [**lb- \_ InsertString**](lb-insertstring.md)-, [**lb \_**](lb-dir.md)-und [**lb- \_ AddFile**](lb-addfile.md) -Nachrichten die kürzeste Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="1f870-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="1f870-123">Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f870-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="1f870-124">Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.</span><span class="sxs-lookup"><span data-stu-id="1f870-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f870-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f870-125">Requirements</span></span>



| <span data-ttu-id="1f870-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f870-126">Requirement</span></span> | <span data-ttu-id="1f870-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1f870-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f870-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f870-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1f870-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f870-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1f870-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f870-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1f870-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f870-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f870-132">Header</span><span class="sxs-lookup"><span data-stu-id="1f870-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f870-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1f870-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f870-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f870-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f870-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1f870-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f870-136">**LB- \_ AddFile**</span><span class="sxs-lookup"><span data-stu-id="1f870-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="1f870-137">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="1f870-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="1f870-138">**LB- \_ dir**</span><span class="sxs-lookup"><span data-stu-id="1f870-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="1f870-139">**LB- \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="1f870-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





