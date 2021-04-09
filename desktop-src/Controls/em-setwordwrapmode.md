---
title: EM_SETWORDWRAPMODE Meldung (RichEdit. h)
description: Legt die Optionen für Wort Umbruch und Wörter Trennung für ein Rich-Edit-Steuerelement fest.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Windows-Steuerelemente für EM_SETWORDWRAPMODE Meldung
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040721"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="40f3e-104">EM \_ setwordwrapmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="40f3e-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="40f3e-105">Legt die Optionen für Wort Umbruch und Wörter Trennung für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="40f3e-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="40f3e-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40f3e-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="40f3e-107">Sie wird in späteren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40f3e-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="40f3e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40f3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f3e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40f3e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40f3e-110">Gibt einen oder mehrere der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="40f3e-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="40f3e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="40f3e-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="40f3e-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="40f3e-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="40f3e-113"><dt>**WBF- \_ WordWrap**</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="40f3e-114">Ermöglicht asiatische-spezifische Zeilenumbruch Vorgänge, wie z. b. Kinsoku in Japanisch.</span><span class="sxs-lookup"><span data-stu-id="40f3e-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="40f3e-115"><dt>**WBF- \_ WordBreak**</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="40f3e-116">Ermöglicht englische Wörter brechende Vorgänge in Japanisch und Chinesisch.</span><span class="sxs-lookup"><span data-stu-id="40f3e-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="40f3e-117">Aktiviert den Vorgang zum Durchsuchen von Hangeul-Wörtern.</span><span class="sxs-lookup"><span data-stu-id="40f3e-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="40f3e-118"><dt>**WBF- \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="40f3e-119">Erkennt eine Überlauf Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="40f3e-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="40f3e-120">(Wird zurzeit nicht unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="40f3e-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="40f3e-121"><dt>**WBF- \_ Level1**</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="40f3e-122">Legt die Satzzeichen Tabelle der Ebene 1 als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="40f3e-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="40f3e-123"><dt>**WBF- \_ Level2**</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="40f3e-124">Legt die Satzzeichen Tabelle der Ebene 2 als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="40f3e-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="40f3e-125"><dt>**\_benutzerdefiniertes WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="40f3e-126">Legt die Anwendungs definierte Interpunktions Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="40f3e-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="40f3e-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40f3e-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40f3e-128">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="40f3e-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f3e-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40f3e-129">Return value</span></span>

<span data-ttu-id="40f3e-130">Diese Meldung gibt die aktuellen Optionen für Wort Umbruch und Wörter Trennung zurück.</span><span class="sxs-lookup"><span data-stu-id="40f3e-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f3e-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40f3e-131">Remarks</span></span>

<span data-ttu-id="40f3e-132">Diese Nachricht darf nicht von der von der Anwendung definierten Wörter Trennung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f3e-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f3e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40f3e-133">Requirements</span></span>



| <span data-ttu-id="40f3e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40f3e-134">Requirement</span></span> | <span data-ttu-id="40f3e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="40f3e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40f3e-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40f3e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="40f3e-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40f3e-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40f3e-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40f3e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="40f3e-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40f3e-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40f3e-140">Header</span><span class="sxs-lookup"><span data-stu-id="40f3e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f3e-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f3e-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





