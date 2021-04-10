---
title: BCM_SETSHIELD Meldung (kommstrg. h)
description: Legt den Status der erhöhten Rechte für eine angegebene Schaltfläche oder einen Befehls Link fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Senden Sie diese Nachricht explizit oder mithilfe des Schaltflächen-Makros "" \_ .
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Windows-Steuerelemente für BCM_SETSHIELD Meldung
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103490"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="33dcc-105">BCM- \_ SETSHIELD-Nachricht</span><span class="sxs-lookup"><span data-stu-id="33dcc-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="33dcc-106">Legt den Status der erhöhten Rechte für eine angegebene Schaltfläche oder einen Befehls Link fest, um ein Symbol mit erhöhten Rechten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="33dcc-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="33dcc-107">Senden Sie diese Nachricht explizit oder mithilfe des [**Schalt \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) Flächen-Makros "".</span><span class="sxs-lookup"><span data-stu-id="33dcc-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33dcc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="33dcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33dcc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33dcc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33dcc-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="33dcc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="33dcc-111">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33dcc-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33dcc-112">Ein **boolescher** Wert, der **true** ist, wenn ein Symbol mit erhöhten Rechten gezeichnet werden soll, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="33dcc-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33dcc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33dcc-113">Return value</span></span>

<span data-ttu-id="33dcc-114">Gibt 1 zurück, wenn erfolgreich, oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="33dcc-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="33dcc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33dcc-115">Remarks</span></span>

<span data-ttu-id="33dcc-116">Um diese Funktionalität nutzen zu können, muss eine Anwendung für die Verwendung comctl32.dll Version 6 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="33dcc-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="33dcc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33dcc-117">Requirements</span></span>



| <span data-ttu-id="33dcc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33dcc-118">Requirement</span></span> | <span data-ttu-id="33dcc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="33dcc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33dcc-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33dcc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33dcc-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33dcc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33dcc-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33dcc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33dcc-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33dcc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33dcc-124">Header</span><span class="sxs-lookup"><span data-stu-id="33dcc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33dcc-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="33dcc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





