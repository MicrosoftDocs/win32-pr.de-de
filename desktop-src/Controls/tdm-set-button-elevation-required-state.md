---
title: TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE Meldung (kommstrg. h)
description: Gibt an, ob eine angegebene Aufgaben Dialogfeld-oder Befehls Verknüpfung über ein Schild Symbol der Benutzerkontensteuerung (UAC) verfügen soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Windows-Steuerelemente für TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE Meldung
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105974"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="582d9-104">TDM \_ - \_ Schaltflächen Erweiterung \_ \_ erforderliche \_ Zustands Meldung</span><span class="sxs-lookup"><span data-stu-id="582d9-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="582d9-105">Gibt an, ob eine angegebene Aufgaben Dialogfeld-oder Befehls Verknüpfung über ein Schild Symbol der Benutzerkontensteuerung (UAC) verfügen soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="582d9-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="582d9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="582d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="582d9-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="582d9-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="582d9-108">Die ID der zu aktualisierenden pushschaltfläche oder des Befehls Links.</span><span class="sxs-lookup"><span data-stu-id="582d9-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="582d9-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="582d9-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="582d9-110">Legen Sie den Wert auf 0 fest, um anzugeben, dass die von der Schaltfläche aufgerufene Aktion keine Erhöhung erfordert.</span><span class="sxs-lookup"><span data-stu-id="582d9-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="582d9-111">Legen Sie auf ungleich NULL fest, um anzugeben, dass die Aktion eine Erhöhung erfordert.</span><span class="sxs-lookup"><span data-stu-id="582d9-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="582d9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="582d9-112">Return value</span></span>

<span data-ttu-id="582d9-113">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="582d9-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="582d9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="582d9-114">Requirements</span></span>



| <span data-ttu-id="582d9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="582d9-115">Requirement</span></span> | <span data-ttu-id="582d9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="582d9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="582d9-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="582d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="582d9-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="582d9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="582d9-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="582d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="582d9-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="582d9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="582d9-121">Header</span><span class="sxs-lookup"><span data-stu-id="582d9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="582d9-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="582d9-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





