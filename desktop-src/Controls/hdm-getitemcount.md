---
title: HDM_GETITEMCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Elemente in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ GetItemCount-Makro verwenden.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- Windows-Steuerelemente für HDM_GETITEMCOUNT Meldung
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104486"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="82554-105">HDM- \_ GetItemCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="82554-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="82554-106">Ruft die Anzahl der Elemente in einem Header Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="82554-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="82554-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="82554-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="82554-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82554-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82554-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82554-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="82554-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="82554-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="82554-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82554-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="82554-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="82554-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82554-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82554-113">Return value</span></span>

<span data-ttu-id="82554-114">Gibt die Anzahl der Elemente zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="82554-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="82554-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82554-115">Requirements</span></span>



| <span data-ttu-id="82554-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82554-116">Requirement</span></span> | <span data-ttu-id="82554-117">Wert</span><span class="sxs-lookup"><span data-stu-id="82554-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82554-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82554-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82554-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82554-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82554-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82554-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82554-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82554-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82554-122">Header</span><span class="sxs-lookup"><span data-stu-id="82554-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="82554-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="82554-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





