---
title: LVM_GETHEADER Meldung (kommstrg. h)
description: Ruft das Handle für das Header Steuerelement ab, das vom Listenansicht-Steuerelement verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ gederader-Makro verwenden.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- Windows-Steuerelemente für LVM_GETHEADER Meldung
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040176"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="899ea-105">LVM- \_ getheiader-Nachricht</span><span class="sxs-lookup"><span data-stu-id="899ea-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="899ea-106">Ruft das Handle für das Header Steuerelement ab, das vom Listenansicht-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="899ea-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="899ea-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ gederader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="899ea-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="899ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="899ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="899ea-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="899ea-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="899ea-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="899ea-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="899ea-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="899ea-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="899ea-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899ea-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="899ea-113">Return value</span></span>

<span data-ttu-id="899ea-114">Gibt das Handle für das Header Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="899ea-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="899ea-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="899ea-115">Requirements</span></span>



| <span data-ttu-id="899ea-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="899ea-116">Requirement</span></span> | <span data-ttu-id="899ea-117">Wert</span><span class="sxs-lookup"><span data-stu-id="899ea-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="899ea-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="899ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="899ea-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="899ea-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="899ea-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="899ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="899ea-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="899ea-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="899ea-122">Header</span><span class="sxs-lookup"><span data-stu-id="899ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="899ea-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="899ea-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





