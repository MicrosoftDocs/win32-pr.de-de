---
title: TDM_SET_PROGRESS_BAR_STATE Meldung (kommstrg. h)
description: Legt den Zustand der Statusanzeige in einem Aufgaben Dialogfeld fest.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- Windows-Steuerelemente für TDM_SET_PROGRESS_BAR_STATE Meldung
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "104352038"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="0e8c4-104">TDM \_ - \_ \_ \_ Statusmeldung "Statusleiste festlegen"</span><span class="sxs-lookup"><span data-stu-id="0e8c4-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="0e8c4-105">Legt den Zustand der Statusanzeige in einem Aufgaben Dialogfeld fest.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e8c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8c4-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e8c4-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8c4-108">Ein **int** -Wert, der den Status der Statusanzeige angibt.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="0e8c4-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0e8c4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0e8c4-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="0e8c4-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0e8c4-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="0e8c4-112"><dt>**PBST \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c4-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="0e8c4-113">Legt die Statusanzeige auf den normalen Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="0e8c4-114"><dt>**PBST \_ angehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c4-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="0e8c4-115">Legt die Statusanzeige auf den angehaltenen Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="0e8c4-116"><dt>**PBST- \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c4-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="0e8c4-117">Legen Sie die Statusanzeige auf den Fehlerstatus fest.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="0e8c4-118">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e8c4-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8c4-119">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8c4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e8c4-120">Return value</span></span>

<span data-ttu-id="0e8c4-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0e8c4-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="0e8c4-122">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="0e8c4-123">Um erweiterte Fehlerinformationen abzurufen, nennen Sie GetLastError.</span><span class="sxs-lookup"><span data-stu-id="0e8c4-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8c4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e8c4-124">Requirements</span></span>



| <span data-ttu-id="0e8c4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e8c4-125">Requirement</span></span> | <span data-ttu-id="0e8c4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0e8c4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8c4-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e8c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8c4-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e8c4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e8c4-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e8c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8c4-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e8c4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e8c4-131">Header</span><span class="sxs-lookup"><span data-stu-id="0e8c4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e8c4-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c4-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





