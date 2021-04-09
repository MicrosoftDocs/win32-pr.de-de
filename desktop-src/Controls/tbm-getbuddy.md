---
title: TBM_GETBUDDY Meldung (kommstrg. h)
description: Ruft das Handle für ein Fenster des TrackBar-Steuerelement-Steuer Elements an einem angegebenen Speicherort ab. Der angegebene Speicherort ist relativ zur Ausrichtung des Steuer Elements (horizontal oder vertikal).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Windows-Steuerelemente für TBM_GETBUDDY Meldung
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957245"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="9bbb1-105">TBM \_ GetBuddy-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9bbb1-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="9bbb1-106">Ruft das Handle für ein Fenster des TrackBar-Steuerelement-Steuer Elements an einem angegebenen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="9bbb1-107">Der angegebene Speicherort ist relativ zur Ausrichtung des Steuer Elements (horizontal oder vertikal).</span><span class="sxs-lookup"><span data-stu-id="9bbb1-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="9bbb1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bbb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bbb1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bbb1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bbb1-110">Ein Wert, der angibt, welches Adress Fenster Handle von relativer Position abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="9bbb1-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9bbb1-111">This value can be one of the following:</span></span>



| <span data-ttu-id="9bbb1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9bbb1-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="9bbb1-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9bbb1-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="9bbb1-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9bbb1-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="9bbb1-115">Ruft das Handle für den Kumpel Links von der TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="9bbb1-116">Wenn das TrackBar-Steuerelement den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, ruft die Nachricht den Kumpel über der TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="9bbb1-117"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9bbb1-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="9bbb1-118">Ruft das Handle für den Buddy rechts von der TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="9bbb1-119">Wenn das TrackBar-Steuerelement den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, ruft die Nachricht den Kumpel unterhalb der TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9bbb1-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bbb1-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9bbb1-121">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bbb1-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bbb1-122">Return value</span></span>

<span data-ttu-id="9bbb1-123">Gibt das Handle für das Buddy-Fenster an der von *wParam* angegebenen Position zurück, oder **null** , wenn kein Buddy-Fenster an dieser Stelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9bbb1-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbb1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bbb1-124">Requirements</span></span>



| <span data-ttu-id="9bbb1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bbb1-125">Requirement</span></span> | <span data-ttu-id="9bbb1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9bbb1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbb1-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bbb1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9bbb1-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bbb1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bbb1-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bbb1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9bbb1-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bbb1-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9bbb1-131">Header</span><span class="sxs-lookup"><span data-stu-id="9bbb1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bbb1-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bbb1-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





