---
title: LB_GETITEMDATA Meldung (Winuser. h)
description: Ruft den Anwendungs definierten Wert ab, der dem angegebenen Listenfeld Element zugeordnet ist.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Windows-Steuerelemente für LB_GETITEMDATA Meldung
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105992"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="7e0fd-104">LB- \_ GetItemData-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7e0fd-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="7e0fd-105">Ruft den Anwendungs definierten Wert ab, der dem angegebenen Listenfeld Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e0fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e0fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e0fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e0fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e0fd-108">Der Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-108">The index of the item.</span></span>

<span data-ttu-id="7e0fd-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="7e0fd-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="7e0fd-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="7e0fd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e0fd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e0fd-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e0fd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e0fd-114">Return value</span></span>

<span data-ttu-id="7e0fd-115">Der Rückgabewert ist der Wert, der dem Element zugeordnet ist, oder lb \_ Err, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="7e0fd-116">Wenn sich das Element in einem vom Besitzer gezeichneten Listenfeld befindet und ohne den [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde, war dieser Wert im *LPARAM* -Parameter der [**lb- \_ AddString**](lb-addstring.md) -oder der [**lb- \_ InsertString**](lb-insertstring.md) -Nachricht enthalten, die das Element dem Listenfeld hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="7e0fd-117">Andernfalls ist es der Wert im *LPARAM* der LB-Nachricht [**\_**](lb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="7e0fd-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0fd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e0fd-118">Requirements</span></span>



| <span data-ttu-id="7e0fd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e0fd-119">Requirement</span></span> | <span data-ttu-id="7e0fd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7e0fd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0fd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e0fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e0fd-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e0fd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e0fd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e0fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e0fd-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e0fd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e0fd-125">Header</span><span class="sxs-lookup"><span data-stu-id="7e0fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e0fd-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7e0fd-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e0fd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e0fd-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e0fd-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e0fd-129">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="7e0fd-130">**LB- \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="7e0fd-131">**LB- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="7e0fd-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 





