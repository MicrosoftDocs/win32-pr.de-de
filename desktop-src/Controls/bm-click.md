---
title: BM_CLICK Meldung (Winuser. h)
description: Simuliert den Benutzer, der auf eine Schaltfläche klickt. Diese Meldung bewirkt, dass die Schaltfläche die \_ lbuttondown-und die WM \_ -lbuttonup-Meldungen empfängt \_
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Windows-Steuerelemente für BM_CLICK Meldung
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040314"
---
# <a name="bm_click-message"></a><span data-ttu-id="7d388-105">BM- \_ Click-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7d388-105">BM\_CLICK message</span></span>

<span data-ttu-id="7d388-106">Simuliert den Benutzer, der auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="7d388-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="7d388-107">Diese Meldung bewirkt, dass die Schaltfläche [**die \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -und die [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldungen empfängt [ \_](bn-clicked.md)</span><span class="sxs-lookup"><span data-stu-id="7d388-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d388-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d388-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d388-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d388-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d388-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7d388-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d388-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d388-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d388-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7d388-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d388-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d388-113">Return value</span></span>

<span data-ttu-id="7d388-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d388-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d388-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d388-115">Remarks</span></span>

<span data-ttu-id="7d388-116">Wenn sich die Schaltfläche in einem Dialogfeld befindet und das Dialogfeld nicht aktiv ist, kann die **BM- \_ Click** -Nachricht fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7d388-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="7d388-117">Um den Erfolg in dieser Situation zu gewährleisten, müssen **\_ Sie** [**die Funktion "" in der Funktion**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) "" von "".</span><span class="sxs-lookup"><span data-stu-id="7d388-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d388-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d388-118">Requirements</span></span>



| <span data-ttu-id="7d388-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d388-119">Requirement</span></span> | <span data-ttu-id="7d388-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7d388-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d388-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d388-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d388-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d388-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d388-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d388-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d388-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d388-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d388-125">Header</span><span class="sxs-lookup"><span data-stu-id="7d388-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d388-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7d388-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

