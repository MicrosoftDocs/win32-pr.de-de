---
title: LVM_SETSELECTEDCOLUMN Meldung (kommstrg. h)
description: Legt den Index der ausgewählten Spalte fest.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- Windows-Steuerelemente für LVM_SETSELECTEDCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859351"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="b30bf-104">LVM- \_ setselectedcolumn-Meldung</span><span class="sxs-lookup"><span data-stu-id="b30bf-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="b30bf-105">Legt den Index der ausgewählten Spalte fest.</span><span class="sxs-lookup"><span data-stu-id="b30bf-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="b30bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b30bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b30bf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b30bf-108">Der Wert vom Typ **int** , der den Spalten Index angibt.</span><span class="sxs-lookup"><span data-stu-id="b30bf-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="b30bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b30bf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b30bf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b30bf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30bf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b30bf-111">Return value</span></span>

<span data-ttu-id="b30bf-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b30bf-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b30bf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b30bf-113">Remarks</span></span>

<span data-ttu-id="b30bf-114">Die Spalten Indizes werden in einem **int** -Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b30bf-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="b30bf-115">Siehe den **pucolumns** -Member von [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span><span class="sxs-lookup"><span data-stu-id="b30bf-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="b30bf-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="b30bf-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b30bf-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b30bf-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b30bf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b30bf-118">Requirements</span></span>



| <span data-ttu-id="b30bf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b30bf-119">Requirement</span></span> | <span data-ttu-id="b30bf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b30bf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b30bf-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b30bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b30bf-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b30bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b30bf-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b30bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b30bf-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b30bf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b30bf-125">Header</span><span class="sxs-lookup"><span data-stu-id="b30bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b30bf-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b30bf-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





