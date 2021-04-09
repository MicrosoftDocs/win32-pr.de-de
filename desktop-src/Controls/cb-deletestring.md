---
title: CB_DELETESTRING Meldung (Winuser. h)
description: Löscht eine Zeichenfolge im Listenfeld eines Kombinations Felds.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Windows-Steuerelemente für CB_DELETESTRING Meldung
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106004"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="08177-104">CB \_ deletestring-Meldung</span><span class="sxs-lookup"><span data-stu-id="08177-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="08177-105">Löscht eine Zeichenfolge im Listenfeld eines Kombinations Felds.</span><span class="sxs-lookup"><span data-stu-id="08177-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="08177-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08177-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08177-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08177-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08177-108">Der null basierte Index der zu löschenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="08177-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="08177-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08177-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08177-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="08177-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08177-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08177-111">Return value</span></span>

<span data-ttu-id="08177-112">Der Rückgabewert ist die Anzahl der Zeichen folgen, die in der Liste verbleiben.</span><span class="sxs-lookup"><span data-stu-id="08177-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="08177-113">Wenn der *wParam* -Parameter einen Index angibt, der größer als die Anzahl der Elemente in der Liste ist, lautet der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="08177-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="08177-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08177-114">Remarks</span></span>

<span data-ttu-id="08177-115">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, sendet das System eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung an den Besitzer des Kombinations Felds, sodass die Anwendung alle zusätzlichen Daten freigeben kann, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="08177-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="08177-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08177-116">Requirements</span></span>



| <span data-ttu-id="08177-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08177-117">Requirement</span></span> | <span data-ttu-id="08177-118">Wert</span><span class="sxs-lookup"><span data-stu-id="08177-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08177-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08177-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08177-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08177-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08177-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08177-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08177-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08177-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08177-123">Header</span><span class="sxs-lookup"><span data-stu-id="08177-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08177-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="08177-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08177-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08177-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="08177-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="08177-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08177-127">**CB \_ resetcontent**</span><span class="sxs-lookup"><span data-stu-id="08177-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="08177-128">**WM- \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="08177-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





