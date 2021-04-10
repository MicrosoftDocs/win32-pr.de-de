---
title: HDM_GETORDERARRAY Meldung (kommstrg. h)
description: Ruft die aktuelle Reihenfolge der Elemente in einem Header Steuerelement von links nach rechts ab. Sie können diese Nachricht explizit senden oder das gesenderarray-Header-Header verwenden \_ .
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Windows-Steuerelemente für HDM_GETORDERARRAY Meldung
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103772"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="77961-105">HDM \_ getor Array-Meldung</span><span class="sxs-lookup"><span data-stu-id="77961-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="77961-106">Ruft die aktuelle Reihenfolge der Elemente in einem Header Steuerelement von links nach rechts ab.</span><span class="sxs-lookup"><span data-stu-id="77961-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="77961-107">Sie können diese Nachricht explizit senden oder das [**\_ gesenderarray-Header-Header**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) verwenden.</span><span class="sxs-lookup"><span data-stu-id="77961-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77961-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="77961-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77961-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77961-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77961-110">Die Anzahl der ganzzahligen Elemente, die *LPARAM* enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="77961-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="77961-111">Dieser Wert muss gleich der Anzahl der Elemente im-Steuerelement sein (siehe [**HDM \_ GetItemCount**](hdm-getitemcount.md)).</span><span class="sxs-lookup"><span data-stu-id="77961-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="77961-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77961-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77961-113">Ein Zeiger auf ein Array von ganzen Zahlen, die die Indexwerte für Elemente in der Kopfzeile empfangen.</span><span class="sxs-lookup"><span data-stu-id="77961-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77961-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77961-114">Return value</span></span>

<span data-ttu-id="77961-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, und der Puffer bei *LPARAM* empfängt die Element Nummer für jedes Element im Header-Steuerelement in der Reihenfolge, in der Sie von links nach rechts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77961-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="77961-116">Andernfalls gibt die Meldung 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="77961-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="77961-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77961-117">Remarks</span></span>

<span data-ttu-id="77961-118">Die Anzahl der Elemente in *LPARAM* wird in *wParam* angegeben und muss gleich der Anzahl der Elemente im Steuerelement sein.</span><span class="sxs-lookup"><span data-stu-id="77961-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="77961-119">Im folgenden Code Fragment wird z. b. genügend Arbeitsspeicher für die Indexwerte reserviert.</span><span class="sxs-lookup"><span data-stu-id="77961-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="77961-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77961-120">Requirements</span></span>



| <span data-ttu-id="77961-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77961-121">Requirement</span></span> | <span data-ttu-id="77961-122">Wert</span><span class="sxs-lookup"><span data-stu-id="77961-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77961-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77961-123">Minimum supported client</span></span><br/> | <span data-ttu-id="77961-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77961-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77961-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77961-125">Minimum supported server</span></span><br/> | <span data-ttu-id="77961-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77961-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77961-127">Header</span><span class="sxs-lookup"><span data-stu-id="77961-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="77961-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="77961-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





