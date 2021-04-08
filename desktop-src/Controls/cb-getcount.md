---
title: CB_GETCOUNT Meldung (Winuser. h)
description: Ruft die Anzahl der Elemente im Listenfeld eines Kombinations Felds ab.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Windows-Steuerelemente für CB_GETCOUNT Meldung
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744017"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="8e789-104">CB \_ GetCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8e789-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="8e789-105">Ruft die Anzahl der Elemente im Listenfeld eines Kombinations Felds ab.</span><span class="sxs-lookup"><span data-stu-id="8e789-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e789-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e789-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e789-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e789-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e789-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8e789-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e789-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e789-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e789-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8e789-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e789-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e789-111">Return value</span></span>

<span data-ttu-id="8e789-112">Der Rückgabewert ist die Anzahl der Elemente im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="8e789-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="8e789-113">Wenn ein Fehler auftritt, ist es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="8e789-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e789-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e789-114">Remarks</span></span>

<span data-ttu-id="8e789-115">Der Index ist NULL basiert, sodass die zurückgegebene Anzahl einen Wert größer als der Indexwert des letzten Elements ist.</span><span class="sxs-lookup"><span data-stu-id="8e789-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e789-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e789-116">Requirements</span></span>



| <span data-ttu-id="8e789-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e789-117">Requirement</span></span> | <span data-ttu-id="8e789-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8e789-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e789-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e789-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e789-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e789-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e789-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e789-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e789-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e789-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e789-123">Header</span><span class="sxs-lookup"><span data-stu-id="8e789-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e789-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8e789-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





