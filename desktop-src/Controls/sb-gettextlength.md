---
title: SB_GETTEXTLENGTH Meldung (kommstrg. h)
description: Ruft die Länge des Texts aus dem angegebenen Teil eines Status Fensters in Zeichen ab.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Windows-Steuerelemente für SB_GETTEXTLENGTH Meldung
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956888"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="d7f9a-104">SB \_ getTextLength-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7f9a-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="d7f9a-105">Ruft die Länge des Texts aus dem angegebenen Teil eines Status Fensters in Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7f9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f9a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7f9a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f9a-108">Der null basierte Index des Teils, von dem Text abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="d7f9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7f9a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d7f9a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f9a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7f9a-111">Return value</span></span>

<span data-ttu-id="d7f9a-112">Gibt einen 32-Bit-Wert zurück, der aus 2 16-Bit-Werten besteht.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="d7f9a-113">Das niedrige Wort gibt die Länge des Texts in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="d7f9a-114">Das hohe Wort gibt den Typ des Vorgangs an, mit dem der Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="d7f9a-115">Der Typ kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d7f9a-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="d7f9a-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d7f9a-116">Return code</span></span>                                                                                    | <span data-ttu-id="d7f9a-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7f9a-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7f9a-118"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f9a-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="d7f9a-119">Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Ebene des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="d7f9a-120"><dt>**SBT- \_ Knoten**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f9a-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="d7f9a-121">Der Text wird ohne Rahmen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="d7f9a-122"><dt>**SBT-Besitzer \_ Zeichnen**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f9a-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="d7f9a-123">Der Text wird vom übergeordneten Fenster gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="d7f9a-124"><dt>**SBT- \_ Popout**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f9a-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="d7f9a-125">Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="d7f9a-126"><dt>**SBT \_ RtlReading**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f9a-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="d7f9a-127">Der Text wird in umgekehrter Richtung zum Text im übergeordneten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7f9a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7f9a-128">Remarks</span></span>

<span data-ttu-id="d7f9a-129">Normaler Windows-Anzeige Text von links nach rechts (LTR).</span><span class="sxs-lookup"><span data-stu-id="d7f9a-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="d7f9a-130">Windows kann so *gespiegelt* werden, dass Sprachen wie Hebräisch oder Arabisch angezeigt werden, die von rechts nach links (RTL) gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="d7f9a-131">Wenn SBT \_ RtlReading festgelegt ist, wird der angegebene Statusfenster Text in umgekehrter Richtung aus dem Text im übergeordneten Fenster gelesen.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="d7f9a-132">Diese Meldung gibt eine maximale Zeichen folgen Länge von 65.535 Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="d7f9a-133">Wenn die tatsächliche Text Zeichenfolge länger ist, wird Sie von der [**SB \_ gettext**](sb-gettext.md) -Nachricht abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="d7f9a-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f9a-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f9a-134">Requirements</span></span>



| <span data-ttu-id="d7f9a-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7f9a-135">Requirement</span></span> | <span data-ttu-id="d7f9a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f9a-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f9a-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7f9a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f9a-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f9a-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7f9a-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7f9a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f9a-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f9a-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7f9a-141">Header</span><span class="sxs-lookup"><span data-stu-id="d7f9a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f9a-142"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f9a-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d7f9a-143">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d7f9a-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7f9a-144">**SB \_ Gettextlengthw** (Unicode) und **SB \_ gettextlengtha** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7f9a-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 





