---
title: CB_GETITEMDATA Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ GetItemData-Nachricht an ein Kombinations Feld, um den von der Anwendung bereitgestellten Wert abzurufen, der mit dem angegebenen Element im Kombinations Feld verknüpft ist.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- Windows-Steuerelemente für CB_GETITEMDATA Meldung
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741456"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="3c6a2-104">CB \_ GetItemData-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3c6a2-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="3c6a2-105">Eine Anwendung sendet eine **CB \_ GetItemData** -Nachricht an ein Kombinations Feld, um den von der Anwendung bereitgestellten Wert abzurufen, der mit dem angegebenen Element im Kombinations Feld verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3c6a2-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c6a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c6a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c6a2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c6a2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6a2-108">Der nullbasierte Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="3c6a2-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="3c6a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c6a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6a2-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c6a2-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c6a2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c6a2-111">Return value</span></span>

<span data-ttu-id="3c6a2-112">Der Rückgabewert ist der Wert, der dem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3c6a2-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="3c6a2-113">Wenn ein Fehler auftritt, ist es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3c6a2-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="3c6a2-114">Wenn sich das Element in einem von einem Besitzer gezeichneten Kombinations Feld befindet, das ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellt wurde, ist der Rückgabewert der Wert, der im *LPARAM* -Parameter der [**CB \_ AddString**](cb-addstring.md) -oder [**CB \_ InsertString**](cb-insertstring.md) -Nachricht enthalten ist, die das Element dem Kombinations Feld hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="3c6a2-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="3c6a2-115">Wenn der **CBS \_ hasstrings** -Stil nicht verwendet wurde, ist der Rückgabewert der *LPARAM* -Parameter in einer [**CB \_ -Nachricht**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3c6a2-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c6a2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c6a2-116">Requirements</span></span>



| <span data-ttu-id="3c6a2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c6a2-117">Requirement</span></span> | <span data-ttu-id="3c6a2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3c6a2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6a2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c6a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c6a2-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c6a2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c6a2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c6a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c6a2-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c6a2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c6a2-123">Header</span><span class="sxs-lookup"><span data-stu-id="3c6a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c6a2-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3c6a2-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c6a2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c6a2-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c6a2-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3c6a2-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c6a2-127">**CB \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="3c6a2-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="3c6a2-128">**CB \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="3c6a2-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3c6a2-129">**CB- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="3c6a2-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 





