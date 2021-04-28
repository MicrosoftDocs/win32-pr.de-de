---
title: TB_GETUNICODEFORMAT Nachricht (Commctrl.h)
description: 'TB_GETUNICODEFORMAT Meldung: Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.'
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4beb5a5ff0b71dd76c85db2788d9dc91aa9f4957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106788"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="d8b05-104">TB \_ GETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d8b05-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="d8b05-105">Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="d8b05-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8b05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8b05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8b05-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d8b05-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d8b05-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d8b05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8b05-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d8b05-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d8b05-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b05-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8b05-111">Return value</span></span>

<span data-ttu-id="d8b05-112">Gibt das Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="d8b05-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="d8b05-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d8b05-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="d8b05-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d8b05-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b05-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8b05-115">Remarks</span></span>

<span data-ttu-id="d8b05-116">Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="d8b05-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b05-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8b05-117">Requirements</span></span>



| <span data-ttu-id="d8b05-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8b05-118">Requirement</span></span> | <span data-ttu-id="d8b05-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d8b05-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b05-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8b05-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b05-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8b05-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8b05-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8b05-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b05-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8b05-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8b05-124">Header</span><span class="sxs-lookup"><span data-stu-id="d8b05-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b05-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b05-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b05-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8b05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b05-127">**TB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d8b05-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





