---
description: Benachrichtigt das Fenster, wenn der Text Eingabebereich geöffnet wird.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: MICROSOFT_TIP_OPENING_MSG Meldung ("Pendel Panel. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372492"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="f936d-103">\_Meldung zum \_ Öffnen der \_ Nachricht von Microsoft Tip</span><span class="sxs-lookup"><span data-stu-id="f936d-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="f936d-104">Benachrichtigt das Fenster, wenn der Text Eingabebereich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f936d-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="f936d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f936d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f936d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f936d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f936d-107">Wird derzeit nicht verwendet, sollte **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f936d-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f936d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f936d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f936d-109">Wird derzeit nicht verwendet, sollte **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f936d-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f936d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f936d-110">Return value</span></span>

<span data-ttu-id="f936d-111">Anwendungen sollten [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nach der Verarbeitung dieser Nachricht anrufen.</span><span class="sxs-lookup"><span data-stu-id="f936d-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="f936d-112">Weitere Informationen zu den Rückgabe Werten finden Sie unter **defwindowproc** .</span><span class="sxs-lookup"><span data-stu-id="f936d-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f936d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f936d-113">Remarks</span></span>

<span data-ttu-id="f936d-114">Diese Benachrichtigung informiert Sie, wenn der Eingabebereich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f936d-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="f936d-115">Wenn Sie in diesem Fall eine Aktion durchführen möchten, behandeln Sie die Nachricht, führen Sie den Vorgang im Handler aus, und übergeben Sie die Nachricht dann an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="f936d-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="f936d-116">Diese Meldung wird auch gesendet, wenn der Text Eingabebereich bereits sichtbar ist und der Benutzer von der Tastatur zur Handschrift Skin wechselt.</span><span class="sxs-lookup"><span data-stu-id="f936d-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f936d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f936d-117">Requirements</span></span>



| <span data-ttu-id="f936d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f936d-118">Requirement</span></span> | <span data-ttu-id="f936d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f936d-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f936d-120">Client</span><span class="sxs-lookup"><span data-stu-id="f936d-120">Client</span></span><br/> | <span data-ttu-id="f936d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f936d-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="f936d-122">Header</span><span class="sxs-lookup"><span data-stu-id="f936d-122">Header</span></span><br/> | <dl> <span data-ttu-id="f936d-123"><dt>"Pendel Panel. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f936d-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 

