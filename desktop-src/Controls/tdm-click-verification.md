---
title: TDM_CLICK_VERIFICATION Meldung (kommstrg. h)
description: Simuliert einen Klick auf das Kontrollkästchen Überprüfung eines Aufgaben Dialogfelds, sofern vorhanden.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Windows-Steuerelemente für TDM_CLICK_VERIFICATION Meldung
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102851"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="e420e-104">TDM- \_ Click- \_ Überprüfungs Meldung</span><span class="sxs-lookup"><span data-stu-id="e420e-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="e420e-105">Simuliert einen Klick auf das Kontrollkästchen Überprüfung eines Aufgaben Dialogfelds, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e420e-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="e420e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e420e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e420e-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e420e-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e420e-108">**True** , wenn der Status des Kontrollkästchens als aktiviert festgelegt werden soll. **False** gibt an, dass das Kontrollkästchen deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e420e-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="e420e-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e420e-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e420e-110">**True** , um den Tastaturfokus auf das Kontrollkästchen festzulegen. Andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e420e-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e420e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e420e-111">Return value</span></span>

<span data-ttu-id="e420e-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e420e-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e420e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e420e-113">Requirements</span></span>



| <span data-ttu-id="e420e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e420e-114">Requirement</span></span> | <span data-ttu-id="e420e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e420e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e420e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e420e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e420e-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e420e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e420e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e420e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e420e-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e420e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e420e-120">Header</span><span class="sxs-lookup"><span data-stu-id="e420e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e420e-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e420e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





