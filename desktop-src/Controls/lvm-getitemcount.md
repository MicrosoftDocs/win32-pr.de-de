---
title: LVM_GETITEMCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Elemente in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemCount-Makros senden.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- Windows-Steuerelemente für LVM_GETITEMCOUNT Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742992"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="bd677-105">LVM- \_ GetItemCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bd677-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="bd677-106">Ruft die Anzahl der Elemente in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="bd677-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="bd677-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="bd677-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd677-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd677-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd677-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd677-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd677-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bd677-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd677-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd677-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bd677-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bd677-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd677-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd677-113">Return value</span></span>

<span data-ttu-id="bd677-114">Gibt die Anzahl der Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="bd677-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd677-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd677-115">Requirements</span></span>



| <span data-ttu-id="bd677-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd677-116">Requirement</span></span> | <span data-ttu-id="bd677-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bd677-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd677-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd677-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd677-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd677-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd677-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd677-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd677-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd677-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd677-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd677-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd677-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd677-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





