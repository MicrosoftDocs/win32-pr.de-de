---
title: LVM_GETOUTLINECOLOR Meldung (kommstrg. h)
description: Ruft die Farbe des Rahmens eines Listenansicht-Steuer Elements ab, wenn der \_ \_ Erweiterte Fenster Stil LVS Ex borderselect festgelegt ist.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Windows-Steuerelemente für LVM_GETOUTLINECOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859155"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="393b3-104">LVM \_ getoutlinecolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="393b3-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="393b3-105">Ruft die Farbe des Rahmens eines Listenansicht-Steuer Elements ab, wenn der erweiterte Fenster Stil [**LVS \_ Ex \_ borderselect**](extended-list-view-styles.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="393b3-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="393b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="393b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="393b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="393b3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="393b3-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="393b3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="393b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="393b3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="393b3-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="393b3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="393b3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="393b3-111">Return value</span></span>

<span data-ttu-id="393b3-112">Gibt eine **COLORREF** -Struktur zurück, die die Farbe des Rahmens eines Listenansicht-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="393b3-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="393b3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="393b3-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="393b3-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="393b3-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="393b3-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="393b3-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="393b3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="393b3-116">Requirements</span></span>



| <span data-ttu-id="393b3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="393b3-117">Requirement</span></span> | <span data-ttu-id="393b3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="393b3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="393b3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="393b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="393b3-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="393b3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="393b3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="393b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="393b3-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="393b3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="393b3-123">Header</span><span class="sxs-lookup"><span data-stu-id="393b3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="393b3-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="393b3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





