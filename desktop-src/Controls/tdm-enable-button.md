---
title: TDM_ENABLE_BUTTON Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert eine Schaltfläche "Push" in einem Aufgaben Dialogfeld.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Windows-Steuerelemente für TDM_ENABLE_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343476"
---
# <a name="tdm_enable_button-message"></a><span data-ttu-id="73ba1-104">TDM \_ - \_ Schaltflächen Nachricht aktivieren</span><span class="sxs-lookup"><span data-stu-id="73ba1-104">TDM\_ENABLE\_BUTTON message</span></span>

<span data-ttu-id="73ba1-105">Aktiviert oder deaktiviert eine Schaltfläche "Push" in einem Aufgaben Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="73ba1-105">Enables or disables a push button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="73ba1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73ba1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ba1-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73ba1-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ba1-108">Ein **int** -Wert, der die ID der Push-Schaltfläche angibt, die aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="73ba1-108">An **int** value that specifies the ID of the push button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="73ba1-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73ba1-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ba1-110">Gibt den Schaltflächen Zustand an.</span><span class="sxs-lookup"><span data-stu-id="73ba1-110">Specifies button state.</span></span> <span data-ttu-id="73ba1-111">Auf 0 festlegen, um die Schaltfläche zu deaktivieren. Legen Sie auf ungleich NULL fest, um die Schaltfläche zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="73ba1-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ba1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73ba1-112">Return value</span></span>

<span data-ttu-id="73ba1-113">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="73ba1-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ba1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73ba1-114">Requirements</span></span>



| <span data-ttu-id="73ba1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73ba1-115">Requirement</span></span> | <span data-ttu-id="73ba1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="73ba1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73ba1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73ba1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73ba1-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73ba1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73ba1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73ba1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73ba1-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73ba1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73ba1-121">Header</span><span class="sxs-lookup"><span data-stu-id="73ba1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73ba1-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ba1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





