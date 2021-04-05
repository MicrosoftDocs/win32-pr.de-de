---
title: MCM_SETMAXSELCOUNT Meldung (kommstrg. h)
description: Legt die maximale Anzahl von Tagen fest, die in einem Monatskalender-Steuerelement ausgewählt werden können. Sie können diese Nachricht explizit oder mit dem monthcal \_ setmaxselcount-Makro senden.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- Windows-Steuerelemente für MCM_SETMAXSELCOUNT Meldung
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859243"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="4e859-105">MCM \_ setmaxselcount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4e859-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="4e859-106">Legt die maximale Anzahl von Tagen fest, die in einem Monatskalender-Steuerelement ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="4e859-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="4e859-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ setmaxselcount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="4e859-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e859-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e859-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e859-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e859-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e859-110">Der Wert vom Typ **int** , der so festgelegt wird, dass die maximale Anzahl von Tagen, die ausgewählt werden können, dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e859-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="4e859-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e859-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e859-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4e859-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e859-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e859-113">Return value</span></span>

<span data-ttu-id="4e859-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="4e859-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="4e859-115">Diese Nachricht schlägt fehl, wenn Sie auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e859-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e859-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e859-116">Requirements</span></span>



| <span data-ttu-id="4e859-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e859-117">Requirement</span></span> | <span data-ttu-id="4e859-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4e859-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e859-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e859-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e859-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e859-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e859-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e859-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e859-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e859-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e859-123">Header</span><span class="sxs-lookup"><span data-stu-id="4e859-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e859-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e859-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





