---
title: LVM_GETTILEVIEWINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem Listenansicht-Steuerelement in der Kachel Ansicht ab.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- Windows-Steuerelemente für LVM_GETTILEVIEWINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742984"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="ea487-104">LVM \_ gettileviewinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="ea487-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="ea487-105">Ruft Informationen zu einem Listenansicht-Steuerelement in der Kachel Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="ea487-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea487-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea487-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea487-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea487-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea487-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ea487-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea487-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea487-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ea487-110">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**lvtileviewinfo**</a> -Struktur, die die abgerufenen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="ea487-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea487-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea487-111">Return value</span></span>

<span data-ttu-id="ea487-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea487-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea487-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea487-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea487-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="ea487-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ea487-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea487-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea487-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea487-116">Requirements</span></span>



| <span data-ttu-id="ea487-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea487-117">Requirement</span></span> | <span data-ttu-id="ea487-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ea487-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea487-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea487-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea487-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea487-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea487-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea487-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea487-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea487-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea487-123">Header</span><span class="sxs-lookup"><span data-stu-id="ea487-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea487-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea487-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





