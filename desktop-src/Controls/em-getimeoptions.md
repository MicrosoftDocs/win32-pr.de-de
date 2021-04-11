---
title: EM_GETIMEOPTIONS Meldung (RichEdit. h)
description: Ruft die aktuellen IME-Optionen (Input Method Editor) ab.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Windows-Steuerelemente für EM_GETIMEOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104822"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="3c454-104">EM \_ getIMEOptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="3c454-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="3c454-105">Ruft die aktuellen IME-Optionen (Input Method Editor) ab.</span><span class="sxs-lookup"><span data-stu-id="3c454-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="3c454-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c454-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="3c454-107">Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c454-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="3c454-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c454-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c454-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c454-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c454-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="3c454-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3c454-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c454-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c454-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="3c454-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c454-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c454-113">Return value</span></span>

<span data-ttu-id="3c454-114">Diese Meldung gibt einen oder mehrere der in der Nachricht [**EM \_ setimeoptions**](em-setimeoptions.md) beschriebenen IME-optionsflagwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="3c454-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c454-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c454-115">Requirements</span></span>



| <span data-ttu-id="3c454-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c454-116">Requirement</span></span> | <span data-ttu-id="3c454-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3c454-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c454-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c454-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c454-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c454-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c454-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c454-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c454-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c454-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c454-122">Header</span><span class="sxs-lookup"><span data-stu-id="3c454-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c454-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c454-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c454-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c454-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c454-125">**EM- \_ Zeit Optionen**</span><span class="sxs-lookup"><span data-stu-id="3c454-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





