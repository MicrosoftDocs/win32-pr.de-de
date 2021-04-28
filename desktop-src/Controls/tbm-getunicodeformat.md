---
title: TBM_GETUNICODEFORMAT Meldung (Commctrl.h)
description: 'TBM_GETUNICODEFORMAT Meldung: Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.'
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104088"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="f08fa-104">TBM \_ GETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f08fa-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="f08fa-105">Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f08fa-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f08fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f08fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f08fa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f08fa-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f08fa-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f08fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f08fa-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f08fa-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f08fa-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08fa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f08fa-111">Return value</span></span>

<span data-ttu-id="f08fa-112">Gibt das Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="f08fa-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="f08fa-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f08fa-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="f08fa-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f08fa-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f08fa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f08fa-115">Remarks</span></span>

<span data-ttu-id="f08fa-116">Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="f08fa-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f08fa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f08fa-117">Requirements</span></span>



| <span data-ttu-id="f08fa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f08fa-118">Requirement</span></span> | <span data-ttu-id="f08fa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f08fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f08fa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f08fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f08fa-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f08fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f08fa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f08fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f08fa-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f08fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f08fa-124">Header</span><span class="sxs-lookup"><span data-stu-id="f08fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f08fa-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="f08fa-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f08fa-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f08fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08fa-127">**TBM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="f08fa-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





