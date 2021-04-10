---
title: LB_SETCOUNT Meldung (Winuser. h)
description: Legt die Anzahl von Elementen in einem Listenfeld fest, das mit dem lbs \_ NODATA-Stil erstellt wurde und nicht mit dem lbs \_ hasstrings-Stil erstellt wurde.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Windows-Steuerelemente für LB_SETCOUNT Meldung
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040893"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="afb7e-104">LB- \_ SetCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="afb7e-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="afb7e-105">Legt die Anzahl von Elementen in einem Listenfeld fest, das mit dem [**lbs \_ NODATA**](list-box-styles.md) -Stil erstellt wurde und nicht mit dem [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="afb7e-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="afb7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afb7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb7e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afb7e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afb7e-108">Gibt die neue Anzahl von Elementen im Listenfeld an.</span><span class="sxs-lookup"><span data-stu-id="afb7e-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="afb7e-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="afb7e-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="afb7e-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="afb7e-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="afb7e-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="afb7e-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="afb7e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afb7e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afb7e-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="afb7e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb7e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afb7e-114">Return value</span></span>

<span data-ttu-id="afb7e-115">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="afb7e-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="afb7e-116">Wenn nicht genügend Arbeitsspeicher zum Speichern der Elemente vorhanden ist, lautet der Rückgabewert "lb \_ errspace".</span><span class="sxs-lookup"><span data-stu-id="afb7e-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="afb7e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afb7e-117">Remarks</span></span>

<span data-ttu-id="afb7e-118">Die **lb- \_ SetCount** -Nachricht wird nur von Listenfeldern unterstützt, die mit dem [**lbs \_ NODATA**](list-box-styles.md) -Stil erstellt wurden und nicht mit dem [**lbs \_ hasstrings**](list-box-styles.md) -Stil erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="afb7e-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="afb7e-119">Alle anderen Listenfelder geben lb- \_ Err zurück.</span><span class="sxs-lookup"><span data-stu-id="afb7e-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb7e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afb7e-120">Requirements</span></span>



| <span data-ttu-id="afb7e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afb7e-121">Requirement</span></span> | <span data-ttu-id="afb7e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="afb7e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afb7e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afb7e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="afb7e-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afb7e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="afb7e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afb7e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="afb7e-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afb7e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="afb7e-127">Header</span><span class="sxs-lookup"><span data-stu-id="afb7e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="afb7e-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="afb7e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afb7e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afb7e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb7e-130">**LB- \_ GetCount**</span><span class="sxs-lookup"><span data-stu-id="afb7e-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 





