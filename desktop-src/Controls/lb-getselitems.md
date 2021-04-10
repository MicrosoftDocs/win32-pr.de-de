---
title: LB_GETSELITEMS Meldung (Winuser. h)
description: Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Element Nummern ausgewählter Elemente in einem Listenfeld mit Mehrfachauswahl angeben.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Windows-Steuerelemente für LB_GETSELITEMS Meldung
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956542"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="4fb36-104">LB- \_ getselitems-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4fb36-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="4fb36-105">Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Element Nummern ausgewählter Elemente in einem Listenfeld mit Mehrfachauswahl angeben.</span><span class="sxs-lookup"><span data-stu-id="4fb36-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fb36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fb36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb36-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fb36-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb36-108">Die maximale Anzahl ausgewählter Elemente, deren Element Nummer in den Puffer eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fb36-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="4fb36-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4fb36-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="4fb36-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="4fb36-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="4fb36-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4fb36-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="4fb36-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fb36-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb36-113">Ein Zeiger auf einen Puffer, der groß genug für die Anzahl der vom *wParam* -Parameter angegebenen ganzzahligen Werte ist.</span><span class="sxs-lookup"><span data-stu-id="4fb36-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb36-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fb36-114">Return value</span></span>

<span data-ttu-id="4fb36-115">Der Rückgabewert ist die Anzahl der Elemente, die im Puffer abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4fb36-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="4fb36-116">Wenn das Listenfeld ein Listenfeld für die einfache Auswahl ist, lautet der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="4fb36-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb36-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fb36-117">Requirements</span></span>



| <span data-ttu-id="4fb36-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fb36-118">Requirement</span></span> | <span data-ttu-id="4fb36-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4fb36-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb36-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fb36-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb36-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fb36-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4fb36-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fb36-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb36-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fb36-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4fb36-124">Header</span><span class="sxs-lookup"><span data-stu-id="4fb36-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fb36-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="4fb36-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb36-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb36-127">**LB- \_ getselcount**</span><span class="sxs-lookup"><span data-stu-id="4fb36-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 





