---
title: EM_GETIMECOMPMODE Meldung (RichEdit. h)
description: Ruft den aktuellen IME-Modus (Eingabemethoden-Editor) für ein Rich-Edit-Steuerelement ab.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Windows-Steuerelemente für EM_GETIMECOMPMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477913"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="f0662-104">EM \_ getimecompmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="f0662-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="f0662-105">Ruft den aktuellen IME-Modus (Eingabemethoden-Editor) für ein Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f0662-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0662-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0662-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0662-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0662-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0662-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f0662-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0662-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0662-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0662-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f0662-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0662-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0662-111">Return value</span></span>

<span data-ttu-id="f0662-112">Der Rückgabewert ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="f0662-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="f0662-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f0662-113">Return code</span></span>                                                                                     | <span data-ttu-id="f0662-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0662-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="f0662-115"><dt>**ICM \_ notopen**</dt></span><span class="sxs-lookup"><span data-stu-id="f0662-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="f0662-116">IME ist nicht geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f0662-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="f0662-117"><dt>**ICM \_ LEVEL3**</dt></span><span class="sxs-lookup"><span data-stu-id="f0662-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="f0662-118">True Inline Modus.</span><span class="sxs-lookup"><span data-stu-id="f0662-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="f0662-119"><dt>**ICM \_ Level2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0662-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="f0662-120">Ebene 2.</span><span class="sxs-lookup"><span data-stu-id="f0662-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="f0662-121"><dt>**ICM \_ Level2 \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="f0662-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="f0662-122">Ebene 2,5</span><span class="sxs-lookup"><span data-stu-id="f0662-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="f0662-123"><dt>**ICM \_ Level2 \_ SUI**</dt></span><span class="sxs-lookup"><span data-stu-id="f0662-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="f0662-124">Spezielle Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f0662-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="f0662-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0662-125">Requirements</span></span>



| <span data-ttu-id="f0662-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0662-126">Requirement</span></span> | <span data-ttu-id="f0662-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f0662-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0662-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0662-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f0662-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0662-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0662-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0662-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f0662-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0662-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0662-132">Header</span><span class="sxs-lookup"><span data-stu-id="f0662-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0662-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0662-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





