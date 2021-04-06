---
title: CB_SETITEMDATA Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ SetItemData-Nachricht, um den Wert festzulegen, der mit dem angegebenen Element in einem Kombinations Feld verknüpft ist.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Windows-Steuerelemente für CB_SETITEMDATA Meldung
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859058"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="c06ba-104">CB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="c06ba-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="c06ba-105">Eine Anwendung sendet eine **CB \_ SetItemData** -Nachricht, um den Wert festzulegen, der mit dem angegebenen Element in einem Kombinations Feld verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c06ba-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c06ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c06ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c06ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ba-108">Gibt den NULL basierten Index des Elements an.</span><span class="sxs-lookup"><span data-stu-id="c06ba-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="c06ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c06ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ba-110">Gibt den neuen Wert an, der dem Element zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c06ba-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06ba-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c06ba-111">Return value</span></span>

<span data-ttu-id="c06ba-112">Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c06ba-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c06ba-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c06ba-113">Remarks</span></span>

<span data-ttu-id="c06ba-114">Wenn sich das angegebene Element in einem vom Besitzer gezeichneten Kombinations Feld befindet, das ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellt wurde, ersetzt diese Meldung den Wert im *LPARAM* -Parameter der [**CB \_ AddString**](cb-addstring.md) -oder [**CB \_ InsertString**](cb-insertstring.md) -Nachricht, die das Element dem Kombinations Feld hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="c06ba-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c06ba-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c06ba-115">Requirements</span></span>



| <span data-ttu-id="c06ba-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c06ba-116">Requirement</span></span> | <span data-ttu-id="c06ba-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c06ba-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c06ba-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c06ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c06ba-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c06ba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c06ba-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c06ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c06ba-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c06ba-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c06ba-122">Header</span><span class="sxs-lookup"><span data-stu-id="c06ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c06ba-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c06ba-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06ba-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c06ba-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="c06ba-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c06ba-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c06ba-126">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="c06ba-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="c06ba-127">**CB \_ GetItemData**</span><span class="sxs-lookup"><span data-stu-id="c06ba-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="c06ba-128">**CB \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="c06ba-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





