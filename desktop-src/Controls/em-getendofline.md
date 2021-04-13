---
title: EM_GETENDOFLINE Meldung (kommstrg. h)
description: Ruft das Zeilenendezeichen ab, das verwendet wird, wenn ein LineBreak eingefügt wird. Senden Sie diese Nachricht explizit oder mithilfe des \_ getendosline-Makros bearbeiten.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Windows-Steuerelemente für EM_GETENDOFLINE Meldung
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475573"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="a626a-105">EM \_ getendosline-Meldung</span><span class="sxs-lookup"><span data-stu-id="a626a-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="a626a-106">Ruft das Zeilenendezeichen für ein Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="a626a-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="a626a-107">Senden Sie diese Nachricht explizit oder mithilfe des [**\_ getendosline**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) -Makros bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a626a-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a626a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a626a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a626a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a626a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a626a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a626a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a626a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a626a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a626a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a626a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a626a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a626a-113">Return value</span></span>

<span data-ttu-id="a626a-114">Gibt das Zeilenendezeichen zurück, das vom Bearbeitungs Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a626a-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="a626a-115">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="a626a-115">This can be one of the following values.</span></span>

| <span data-ttu-id="a626a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a626a-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="a626a-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a626a-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="a626a-118"><dt>**EC \_ EndOf line \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="a626a-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="a626a-119">Das Zeilenendezeichen, das für neue lineumbrüche verwendet wird, ist Wagen Rücklauf gefolgt von Zeilenvorschub (CRLF).</span><span class="sxs-lookup"><span data-stu-id="a626a-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="a626a-120"><dt>**EC \_ EndOf line \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="a626a-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="a626a-121">Das Zeilenendezeichen, das für neue lineumbrüche verwendet wird, ist Wagen Rücklauf (CR).</span><span class="sxs-lookup"><span data-stu-id="a626a-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="a626a-122"><dt>**EC \_ endosline \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="a626a-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="a626a-123">Das Zeilenendezeichen, das für neue lineumbrüche verwendet wird, ist Zeilenvorschub (LF).</span><span class="sxs-lookup"><span data-stu-id="a626a-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="a626a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a626a-124">Remarks</span></span>

<span data-ttu-id="a626a-125">Wenn das verwendete Zeilenendezeichen auf **EC \_ EndOfLine \_ detectfromcontent** mithilfe von [**Edit \_ setendofline**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline)festgelegt wird, gibt diese Meldung das erkannte Zeilenendezeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="a626a-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="a626a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a626a-126">Requirements</span></span>



| <span data-ttu-id="a626a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a626a-127">Requirement</span></span> | <span data-ttu-id="a626a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a626a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a626a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a626a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a626a-130">Windows 10, Version 1809, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a626a-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a626a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a626a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a626a-132">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a626a-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a626a-133">Header</span><span class="sxs-lookup"><span data-stu-id="a626a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a626a-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a626a-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a626a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a626a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a626a-136">\**EM- \_ Ziel*</span><span class="sxs-lookup"><span data-stu-id="a626a-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





