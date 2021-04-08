---
title: TDM_ENABLE_RADIO_BUTTON Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgaben Dialogfeld.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- Windows-Steuerelemente für TDM_ENABLE_RADIO_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957098"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="a8ea5-104">TDM-Optionsfeld \_ \_ \_ Nachricht aktivieren</span><span class="sxs-lookup"><span data-stu-id="a8ea5-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="a8ea5-105">Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgaben Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="a8ea5-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8ea5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8ea5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ea5-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8ea5-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ea5-108">Ein **int** -Wert, der die ID des Options Felds angibt, das aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8ea5-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a8ea5-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8ea5-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ea5-110">Gibt den Schaltflächen Zustand an.</span><span class="sxs-lookup"><span data-stu-id="a8ea5-110">Specifies button state.</span></span> <span data-ttu-id="a8ea5-111">Auf 0 festlegen, um die Schaltfläche zu deaktivieren. Legen Sie auf ungleich NULL fest, um die Schaltfläche zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a8ea5-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8ea5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8ea5-112">Return value</span></span>

<span data-ttu-id="a8ea5-113">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a8ea5-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ea5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8ea5-114">Requirements</span></span>



| <span data-ttu-id="a8ea5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8ea5-115">Requirement</span></span> | <span data-ttu-id="a8ea5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a8ea5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ea5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8ea5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ea5-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8ea5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8ea5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8ea5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ea5-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8ea5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8ea5-121">Header</span><span class="sxs-lookup"><span data-stu-id="a8ea5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8ea5-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8ea5-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





