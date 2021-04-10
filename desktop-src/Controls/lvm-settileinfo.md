---
title: LVM_SETTILEINFO Meldung (kommstrg. h)
description: Legt Informationen für eine vorhandene Kachel eines Listenansicht-Steuer Elements fest.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Windows-Steuerelemente für LVM_SETTILEINFO Meldung
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103354"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="43558-104">LVM- \_ settileinfo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="43558-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="43558-105">Legt Informationen für eine vorhandene Kachel eines Listenansicht-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="43558-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="43558-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43558-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43558-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43558-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="43558-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43558-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43558-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="43558-110">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**lvtileinfo**</a> -Struktur, die die festzulegenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="43558-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43558-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43558-111">Return value</span></span>

<span data-ttu-id="43558-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="43558-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="43558-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43558-113">Remarks</span></span>

<span data-ttu-id="43558-114">**LVM \_ Settileingefo** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43558-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="43558-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="43558-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="43558-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="43558-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43558-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43558-117">Requirements</span></span>



| <span data-ttu-id="43558-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43558-118">Requirement</span></span> | <span data-ttu-id="43558-119">Wert</span><span class="sxs-lookup"><span data-stu-id="43558-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43558-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43558-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43558-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43558-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43558-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43558-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43558-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43558-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43558-124">Header</span><span class="sxs-lookup"><span data-stu-id="43558-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43558-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="43558-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





