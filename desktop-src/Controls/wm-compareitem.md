---
title: WM_COMPAREITEM Meldung (Winuser. h)
description: Wird gesendet, um die relative Position eines neuen Elements in der sortierten Liste eines von einem Besitzer gezeichneten Kombinations Felds oder Listen Felds zu bestimmen.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Windows-Steuerelemente für WM_COMPAREITEM Meldung
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475114"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="f8b32-104">WM- \_ compareitem-Meldung</span><span class="sxs-lookup"><span data-stu-id="f8b32-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="f8b32-105">Wird gesendet, um die relative Position eines neuen Elements in der sortierten Liste eines von einem Besitzer gezeichneten Kombinations Felds oder Listen Felds zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f8b32-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="f8b32-106">Jedes Mal, wenn die Anwendung ein neues Element hinzufügt, sendet das System diese Nachricht an den Besitzer eines Kombinations Felds oder eines Listen Felds, das mit der [**CBS- \_ Sortierung**](combo-box-styles.md) oder dem [**lbs- \_ Sortier**](list-box-styles.md) Stil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f8b32-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f8b32-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8b32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b32-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8b32-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8b32-109">Gibt den Bezeichner des Steuer Elements an, das die **WM \_ compareitem** -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="f8b32-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="f8b32-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8b32-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8b32-111">Ein Zeiger auf eine [**compareitemstruct**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) -Struktur, die die Bezeichner und die von der Anwendung bereitgestellten Daten für zwei Elemente im Kombinations-oder Listenfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="f8b32-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b32-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8b32-112">Return value</span></span>

<span data-ttu-id="f8b32-113">Der Rückgabewert gibt die relative Position der beiden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="f8b32-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="f8b32-114">Dies kann ein beliebiger Wert sein, der in der folgenden Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="f8b32-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="f8b32-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f8b32-115">Return code</span></span>                                                                          | <span data-ttu-id="f8b32-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8b32-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="f8b32-117"><dt>**Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b32-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="f8b32-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b32-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="f8b32-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b32-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="f8b32-120">Element 1 ist Element 2 in der sortierten Reihenfolge voraus.</span><span class="sxs-lookup"><span data-stu-id="f8b32-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="f8b32-121"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b32-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="f8b32-122">Die Elemente 1 und 2 sind äquivalent in der sortierten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8b32-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="f8b32-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b32-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="f8b32-124">Element 1 folgt Element 2 in der sortierten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8b32-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="f8b32-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8b32-125">Remarks</span></span>

<span data-ttu-id="f8b32-126">Wenn der Besitzer eines von einem Besitzer gezeichneten Kombinations Felds oder Listen Felds diese Nachricht empfängt, gibt der Besitzer einen Wert zurück, der angibt, welche der durch die [**compareitemstruct**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) -Struktur angegebenen Elemente vor dem anderen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8b32-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="f8b32-127">Normalerweise sendet das System diese Nachricht mehrmals, bis die genaue Position für das neue Element bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="f8b32-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="f8b32-128">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f8b32-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="f8b32-129">Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f8b32-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b32-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8b32-130">Requirements</span></span>



| <span data-ttu-id="f8b32-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8b32-131">Requirement</span></span> | <span data-ttu-id="f8b32-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b32-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b32-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8b32-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b32-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8b32-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f8b32-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8b32-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b32-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8b32-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8b32-137">Header</span><span class="sxs-lookup"><span data-stu-id="f8b32-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b32-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f8b32-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b32-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8b32-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8b32-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f8b32-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8b32-141">**COMPAREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f8b32-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="f8b32-142">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="f8b32-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f8b32-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="f8b32-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

