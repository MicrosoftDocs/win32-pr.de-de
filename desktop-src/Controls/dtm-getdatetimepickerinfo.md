---
title: DTM_GETDATETIMEPICKERINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem DTP-Steuerelement (Datums-und Zeitauswahl) ab.
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Windows-Steuerelemente für DTM_GETDATETIMEPICKERINFO Meldung
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475405"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="0358a-104">DTM \_ getdatetimepickerinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="0358a-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="0358a-105">Ruft Informationen zu einem DTP-Steuerelement (Datums-und Zeitauswahl) ab.</span><span class="sxs-lookup"><span data-stu-id="0358a-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0358a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0358a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0358a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0358a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0358a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0358a-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0358a-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0358a-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="0358a-110">Ein Zeiger auf <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**datetimepickerinfo**</a> , um die Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0358a-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="0358a-111">Der Aufrufer ist dafür verantwortlich, den Arbeitsspeicher für diese Struktur zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0358a-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="0358a-112">Legen Sie den **CBSIZE** -Member der-Struktur auf sizeof (datetimepickerinfo) fest, bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="0358a-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0358a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0358a-113">Return value</span></span>

<span data-ttu-id="0358a-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0358a-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0358a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0358a-115">Requirements</span></span>



| <span data-ttu-id="0358a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0358a-116">Requirement</span></span> | <span data-ttu-id="0358a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0358a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0358a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0358a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0358a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0358a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0358a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0358a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0358a-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0358a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0358a-122">Header</span><span class="sxs-lookup"><span data-stu-id="0358a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0358a-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0358a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





