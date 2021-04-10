---
title: LVM_SETOUTLINECOLOR Meldung (kommstrg. h)
description: Legt die Farbe des Rahmens eines Listenansicht-Steuer Elements fest, wenn der \_ \_ Erweiterte Fenster Stil LVS Ex borderselect festgelegt ist.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Windows-Steuerelemente für LVM_SETOUTLINECOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858653"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="ac34b-104">LVM- \_ setoutlinecolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="ac34b-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="ac34b-105">Legt die Farbe des Rahmens eines Listenansicht-Steuer Elements fest, wenn der erweiterte Fenster Stil [**LVS \_ Ex \_ borderselect**](extended-list-view-styles.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac34b-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac34b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac34b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac34b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ac34b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ac34b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ac34b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac34b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ac34b-110">**COLORREF** -Struktur, die die Farbe zum Festlegen des Rahmens angibt.</span><span class="sxs-lookup"><span data-stu-id="ac34b-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac34b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac34b-111">Return value</span></span>

<span data-ttu-id="ac34b-112">Gibt eine **COLORREF** -Struktur zurück, die die Kontur Farbe enthält.</span><span class="sxs-lookup"><span data-stu-id="ac34b-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac34b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac34b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac34b-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="ac34b-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ac34b-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ac34b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac34b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac34b-116">Requirements</span></span>



| <span data-ttu-id="ac34b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac34b-117">Requirement</span></span> | <span data-ttu-id="ac34b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ac34b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac34b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac34b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac34b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac34b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac34b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac34b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac34b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac34b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac34b-123">Header</span><span class="sxs-lookup"><span data-stu-id="ac34b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac34b-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac34b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





