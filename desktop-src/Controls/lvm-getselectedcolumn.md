---
title: LVM_GETSELECTEDCOLUMN Meldung (kommstrg. h)
description: Ruft eine Ganzzahl ab, die die ausgewählte Spalte angibt.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- Windows-Steuerelemente für LVM_GETSELECTEDCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340998"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="c0c1b-104">LVM \_ getSelectedColumn-Meldung</span><span class="sxs-lookup"><span data-stu-id="c0c1b-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="c0c1b-105">Ruft eine Ganzzahl ab, die die ausgewählte Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="c0c1b-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0c1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0c1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c1b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0c1b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0c1b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c0c1b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c0c1b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0c1b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0c1b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c0c1b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c1b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0c1b-111">Return value</span></span>

<span data-ttu-id="c0c1b-112">Gibt einen **uint** -Wert zurück, der die ausgewählte Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="c0c1b-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c1b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0c1b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0c1b-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="c0c1b-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c0c1b-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0c1b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0c1b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0c1b-116">Requirements</span></span>



| <span data-ttu-id="c0c1b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0c1b-117">Requirement</span></span> | <span data-ttu-id="c0c1b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c0c1b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c1b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0c1b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c1b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0c1b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0c1b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0c1b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c1b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0c1b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0c1b-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0c1b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0c1b-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c1b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





