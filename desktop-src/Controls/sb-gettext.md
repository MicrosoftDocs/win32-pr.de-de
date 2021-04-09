---
title: SB_GETTEXT Meldung (kommstrg. h)
description: Ruft den Text aus dem angegebenen Teil eines Status Fensters ab.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Windows-Steuerelemente für SB_GETTEXT Meldung
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040845"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="3f046-104">SB \_ gettext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3f046-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="3f046-105">Ruft den Text aus dem angegebenen Teil eines Status Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="3f046-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f046-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f046-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f046-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f046-108">Der null basierte Index des Teils, von dem Text abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f046-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="3f046-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f046-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f046-110">Ein Zeiger auf den Puffer, der den Text als eine mit NULL endenden Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="3f046-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="3f046-111">Verwenden Sie die [**SB \_ getTextLength**](sb-gettextlength.md) -Nachricht, um die erforderliche Größe des Puffers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3f046-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f046-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f046-112">Return value</span></span>

<span data-ttu-id="3f046-113">Gibt einen 32-Bit-Wert zurück, der aus 2 16-Bit-Werten besteht.</span><span class="sxs-lookup"><span data-stu-id="3f046-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="3f046-114">Das niedrige Wort gibt die Länge des Texts in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="3f046-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="3f046-115">Das hohe Wort gibt den Typ des Vorgangs an, mit dem der Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f046-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="3f046-116">Der Typ kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3f046-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="3f046-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3f046-117">Return code</span></span>                                                                                    | <span data-ttu-id="3f046-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f046-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f046-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3f046-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="3f046-120">Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Ebene des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3f046-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="3f046-121"><dt>**SBT- \_ Knoten**</dt></span><span class="sxs-lookup"><span data-stu-id="3f046-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="3f046-122">Der Text wird ohne Rahmen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f046-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="3f046-123"><dt>**SBT- \_ Popout**</dt></span><span class="sxs-lookup"><span data-stu-id="3f046-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="3f046-124">Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3f046-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="3f046-125"><dt>**SBT \_ RtlReading**</dt></span><span class="sxs-lookup"><span data-stu-id="3f046-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="3f046-126">Der Text wird in umgekehrter Richtung des Texts im übergeordneten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f046-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="3f046-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f046-127">Remarks</span></span>

<span data-ttu-id="3f046-128">**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="3f046-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="3f046-129">Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen.</span><span class="sxs-lookup"><span data-stu-id="3f046-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="3f046-130">Wenn Sie diese Meldung verwenden, rufen Sie zunächst [**SB \_ getTextLength**](sb-gettextlength.md) auf, um die erforderliche Anzahl von Zeichen abzurufen, und rufen Sie dann die Nachricht auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3f046-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="3f046-131">Wenn Sie warten, bis **SB \_ gettext** aufgerufen wird, kann sich der Text ändern, wodurch der Rückgabewert von **SB \_ getTextLength** ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="3f046-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="3f046-132">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3f046-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="3f046-133">Diese Meldung gibt maximal 65.535 Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="3f046-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="3f046-134">Wenn die Text Zeichenfolge länger als die Zeichenfolge ist, wird Sie abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3f046-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="3f046-135">Wenn der Text den Typ SBT \_ -Besitzer zeichnen aufweist, gibt diese Meldung den 32-Bit-Wert zurück, der dem Text anstelle der Länge und dem Vorgangstyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3f046-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="3f046-136">Normaler Windows-Anzeige Text von links nach rechts (LTR).</span><span class="sxs-lookup"><span data-stu-id="3f046-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="3f046-137">Windows kann so *gespiegelt* werden, dass Sprachen wie Hebräisch oder Arabisch angezeigt werden, die von rechts nach links (RTL) gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="3f046-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="3f046-138">Wenn SBT \_ RtlReading festgelegt ist, wird die *LPARAM* -Zeichenfolge in der entgegengesetzten Richtung aus dem Text im übergeordneten Fenster gelesen.</span><span class="sxs-lookup"><span data-stu-id="3f046-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f046-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f046-139">Requirements</span></span>



| <span data-ttu-id="3f046-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f046-140">Requirement</span></span> | <span data-ttu-id="3f046-141">Wert</span><span class="sxs-lookup"><span data-stu-id="3f046-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f046-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f046-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3f046-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f046-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f046-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f046-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3f046-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f046-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f046-146">Header</span><span class="sxs-lookup"><span data-stu-id="3f046-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f046-147"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f046-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3f046-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3f046-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3f046-149">**SB \_ Gettextw** (Unicode) und **SB \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3f046-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="3f046-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f046-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f046-151">**SB- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="3f046-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





