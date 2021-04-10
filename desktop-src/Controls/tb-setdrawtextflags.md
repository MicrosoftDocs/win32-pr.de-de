---
title: TB_SETDRAWTEXTFLAGS Meldung (kommstrg. h)
description: Legt die textzeichenflags für die Symbolleiste fest.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Windows-Steuerelemente für TB_SETDRAWTEXTFLAGS Meldung
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956877"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="95783-104">TB \_ setdrawtextflags-Meldung</span><span class="sxs-lookup"><span data-stu-id="95783-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="95783-105">Legt die textzeichenflags für die Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="95783-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="95783-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95783-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95783-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95783-108">Ein oder mehrere der \_ in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)angegebenen dt-Flags, die angeben, welche Bits in *LPARAM* verwendet werden, wenn der Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="95783-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="95783-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95783-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95783-110">Mindestens eines der \_ in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)angegebenen dt-Flags, die angeben, wie der Schaltflächen Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="95783-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="95783-111">Dieser Wert wird an die **DrawText** -Funktion übermittelt, wenn der Schaltflächen Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="95783-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95783-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95783-112">Return value</span></span>

<span data-ttu-id="95783-113">Gibt die vorherigen textzeichenflags zurück.</span><span class="sxs-lookup"><span data-stu-id="95783-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="95783-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95783-114">Remarks</span></span>

<span data-ttu-id="95783-115">Mit dem *wParam* -Parameter können Sie angeben, welche Flags verwendet werden, wenn der Text gezeichnet wird, auch wenn diese Flags ausgeschaltet sind.</span><span class="sxs-lookup"><span data-stu-id="95783-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="95783-116">Wenn Sie z. b. nicht möchten, dass beim Zeichnen von Text das Flag dt Center \_ verwendet wird, fügen Sie \_ *wParam* das Flag dt Center hinzu, und geben Sie \_ in *LPARAM* nicht das Flag dt Center an.</span><span class="sxs-lookup"><span data-stu-id="95783-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="95783-117">Dadurch wird verhindert, dass das Steuerelement das DT \_ Center-Flag an die [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) -Funktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="95783-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="95783-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95783-118">Requirements</span></span>



| <span data-ttu-id="95783-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95783-119">Requirement</span></span> | <span data-ttu-id="95783-120">Wert</span><span class="sxs-lookup"><span data-stu-id="95783-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95783-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95783-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95783-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95783-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95783-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95783-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95783-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95783-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95783-125">Header</span><span class="sxs-lookup"><span data-stu-id="95783-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="95783-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="95783-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

