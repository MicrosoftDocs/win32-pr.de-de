---
title: EM_SETENDOFLINE Meldung (kommstrg. h)
description: Legt das Zeilenendezeichen fest, das verwendet wird, wenn ein LineBreak eingefügt wird.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Windows-Steuerelemente für EM_SETENDOFLINE Meldung
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478570"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="dfb65-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="dfb65-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="dfb65-105">Legt das Zeilenendezeichen fest, das verwendet wird, wenn ein LineBreak eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dfb65-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="dfb65-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfb65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb65-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfb65-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfb65-108">Gibt das Zeilenendezeichen an, das beim Einfügen eines LineBreak-Zeichens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfb65-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="dfb65-109">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="dfb65-109">This can be one of the following values.</span></span>


| <span data-ttu-id="dfb65-110">Wert</span><span class="sxs-lookup"><span data-stu-id="dfb65-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="dfb65-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dfb65-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="dfb65-112"><dt>**EC \_ endosline \_ detectfromcontent**</dt></span><span class="sxs-lookup"><span data-stu-id="dfb65-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="dfb65-113">Legt das Zeilenendezeichen fest, das für neue lineumbrüche auf das vom aktuellen Dokument verwendete Zeichen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfb65-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="dfb65-114"><dt>**EC \_ EndOf line \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="dfb65-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="dfb65-115">Legt das Zeilenendezeichen fest, das für neue lineumbrüche verwendet wird, gefolgt von Zeilenvorschub (CRLF).</span><span class="sxs-lookup"><span data-stu-id="dfb65-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="dfb65-116"><dt>**EC \_ EndOf line \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="dfb65-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="dfb65-117">Legt das Zeilenendezeichen fest, das für neue lineumbrüche zum Wagen Rücklauf (CR) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfb65-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="dfb65-118"><dt>**EC \_ endosline \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="dfb65-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="dfb65-119">Legt das Zeilenendezeichen fest, das für neue lineumbrüche auf Zeilenvorschub (LF) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfb65-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="dfb65-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfb65-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfb65-121">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dfb65-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb65-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfb65-122">Return value</span></span>

<span data-ttu-id="dfb65-123">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dfb65-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="dfb65-124">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="dfb65-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb65-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfb65-125">Remarks</span></span>

<span data-ttu-id="dfb65-126">Wenn der Zeilenende Zeichensatz **EC \_ EndOfLine \_ detectfromcontent** ist, erkennt das Bearbeitungs Steuerelement nur Zeilenendezeichen, die gemäß seinem erweiterten Fenster Stil unterstützt werden. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="dfb65-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb65-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfb65-127">Requirements</span></span>



| <span data-ttu-id="dfb65-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfb65-128">Requirement</span></span> | <span data-ttu-id="dfb65-129">Wert</span><span class="sxs-lookup"><span data-stu-id="dfb65-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb65-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfb65-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb65-131">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfb65-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfb65-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfb65-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb65-133">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfb65-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dfb65-134">Header</span><span class="sxs-lookup"><span data-stu-id="dfb65-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb65-135"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb65-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb65-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfb65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb65-137">\**EM \_ getendosline*</span><span class="sxs-lookup"><span data-stu-id="dfb65-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 





