---
title: LVM_GETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Ruft die Farbe der Einfügemarke ab.
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- Windows-Steuerelemente für LVM_GETINSERTMARKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106677"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="9df8e-104">LVM \_ getinsertmarkcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="9df8e-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="9df8e-105">Ruft die Farbe der Einfügemarke ab.</span><span class="sxs-lookup"><span data-stu-id="9df8e-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="9df8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9df8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df8e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9df8e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9df8e-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9df8e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9df8e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9df8e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9df8e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9df8e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df8e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9df8e-111">Return value</span></span>

<span data-ttu-id="9df8e-112">Gibt eine **COLORREF** -Struktur zurück, die die Farbe der Einfügemarke enthält.</span><span class="sxs-lookup"><span data-stu-id="9df8e-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df8e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9df8e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9df8e-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="9df8e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9df8e-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9df8e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9df8e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9df8e-116">Requirements</span></span>



| <span data-ttu-id="9df8e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9df8e-117">Requirement</span></span> | <span data-ttu-id="9df8e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9df8e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9df8e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9df8e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9df8e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9df8e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9df8e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9df8e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9df8e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9df8e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9df8e-123">Header</span><span class="sxs-lookup"><span data-stu-id="9df8e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9df8e-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df8e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





