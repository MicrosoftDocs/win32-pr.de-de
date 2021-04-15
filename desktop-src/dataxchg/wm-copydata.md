---
title: WM_COPYDATA Meldung (Winuser. h)
description: Eine Anwendung sendet die Nachricht "WM \_ CopyData", um Daten an eine andere Anwendung zu übergeben.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477178"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="93a05-104">Meldung zum WM- \_ CopyData</span><span class="sxs-lookup"><span data-stu-id="93a05-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="93a05-105">Eine Anwendung sendet die Nachricht " **WM \_ CopyData** ", um Daten an eine andere Anwendung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="93a05-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="93a05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93a05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93a05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93a05-108">Ein Handle für das Fenster, in dem die Daten übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="93a05-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="93a05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93a05-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93a05-110">Ein Zeiger auf eine [**copydatastruct**](/windows/win32/api/winuser/ns-winuser-copydatastruct) -Struktur, die die zu über gebenden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="93a05-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a05-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93a05-111">Return value</span></span>

<span data-ttu-id="93a05-112">Wenn die empfangende Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben. Andernfalls sollte **false** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93a05-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93a05-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93a05-113">Remarks</span></span>

<span data-ttu-id="93a05-114">Die zu über gebenden Daten dürfen keine Zeiger oder andere Verweise auf Objekte enthalten, auf die die Anwendung, die die Daten empfängt, nicht zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="93a05-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="93a05-115">Während diese Nachricht gesendet wird, dürfen die referenzierten Daten nicht von einem anderen Thread des Sendevorgangs geändert werden.</span><span class="sxs-lookup"><span data-stu-id="93a05-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="93a05-116">Die empfangende Anwendung sollte die schreibgeschützten Daten berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="93a05-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="93a05-117">Der *LPARAM* -Parameter ist nur während der Verarbeitung der Nachricht gültig.</span><span class="sxs-lookup"><span data-stu-id="93a05-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="93a05-118">Die empfangende Anwendung sollte den von *LPARAM* referenzierten Speicher nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="93a05-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="93a05-119">Wenn die empfangende Anwendung auf die Daten zugreifen muss, nachdem [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) zurückgegeben wurde, müssen die Daten in einen lokalen Puffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="93a05-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="93a05-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93a05-120">Examples</span></span>

<span data-ttu-id="93a05-121">Ein Beispiel finden Sie unter [Verwenden von Datenkopien](using-data-copy.md).</span><span class="sxs-lookup"><span data-stu-id="93a05-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93a05-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93a05-122">Requirements</span></span>



| <span data-ttu-id="93a05-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93a05-123">Requirement</span></span> | <span data-ttu-id="93a05-124">Wert</span><span class="sxs-lookup"><span data-stu-id="93a05-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a05-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93a05-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93a05-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93a05-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="93a05-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93a05-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93a05-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93a05-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93a05-129">Header</span><span class="sxs-lookup"><span data-stu-id="93a05-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a05-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="93a05-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a05-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93a05-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="93a05-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="93a05-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="93a05-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="93a05-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="93a05-134">**Copydatastruct**</span><span class="sxs-lookup"><span data-stu-id="93a05-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

