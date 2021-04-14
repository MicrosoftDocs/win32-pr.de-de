---
title: EM_STREAMIN Meldung (RichEdit. h)
description: Ersetzt den Inhalt eines Rich-Edit-Steuer Elements durch einen Datenstrom, der von einer Anwendung bereitgestellt wird, die definiert ist \ 8211; Editstreamcallback-Rückruffunktion.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Windows-Steuerelemente für EM_STREAMIN Meldung
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478276"
---
# <a name="em_streamin-message"></a><span data-ttu-id="569a3-104">EM- \_ StreamIn-Meldung</span><span class="sxs-lookup"><span data-stu-id="569a3-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="569a3-105">Ersetzt den Inhalt eines Rich-Edit-Steuer Elements durch einen Datenstrom, der von einer Anwendung bereitgestellt wird, die die [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Rückruffunktion definiert.</span><span class="sxs-lookup"><span data-stu-id="569a3-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="569a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="569a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="569a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="569a3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="569a3-108">Gibt die Datenformat-und Ersetzungs Optionen an.</span><span class="sxs-lookup"><span data-stu-id="569a3-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="569a3-109">Dieser Wert muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="569a3-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="569a3-110">Wert</span><span class="sxs-lookup"><span data-stu-id="569a3-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="569a3-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="569a3-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="569a3-112"><dt>**SF \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="569a3-113">RTF</span><span class="sxs-lookup"><span data-stu-id="569a3-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="569a3-114"><dt>**SF- \_ Text**</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="569a3-115">Text</span><span class="sxs-lookup"><span data-stu-id="569a3-115">Text</span></span><br/> |



 

<span data-ttu-id="569a3-116">Außerdem können Sie die folgenden Flags angeben.</span><span class="sxs-lookup"><span data-stu-id="569a3-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="569a3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="569a3-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="569a3-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="569a3-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="569a3-119"><dt>**SFF- \_ plainrtf**</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="569a3-120">Wenn angegeben, werden nur Schlüsselwörter gestreamt, die allen Sprachen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="569a3-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="569a3-121">Sprachspezifische RTF-Schlüsselwörter im Stream werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="569a3-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="569a3-122">Wenn nicht angegeben, werden alle Schlüsselwörter in gestreamt.</span><span class="sxs-lookup"><span data-stu-id="569a3-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="569a3-123">Sie können dieses Flag mit dem **SF \_ RTF** -Flag kombinieren.</span><span class="sxs-lookup"><span data-stu-id="569a3-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="569a3-124"><dt>**SFF- \_ Auswahl**</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="569a3-125">Wenn angegeben, ersetzt der Datenstrom den Inhalt der aktuellen Auswahl.</span><span class="sxs-lookup"><span data-stu-id="569a3-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="569a3-126">Wenn nicht angegeben, ersetzt der Datenstrom den gesamten Inhalt des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="569a3-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="569a3-127">Sie können dieses Flag mit den **SF- \_ Text** -oder **SF \_ RTF** -Flags kombinieren.</span><span class="sxs-lookup"><span data-stu-id="569a3-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="569a3-128"><dt>**SF ( \_ Unicode)**</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="569a3-129">**Microsoft Rich Edit 2,0 und höher:** Gibt Unicode-Text an.</span><span class="sxs-lookup"><span data-stu-id="569a3-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="569a3-130">Sie können dieses Flag mit dem **SF- \_ textflag** kombinieren.</span><span class="sxs-lookup"><span data-stu-id="569a3-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="569a3-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="569a3-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="569a3-132">Zeiger auf eine [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="569a3-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="569a3-133">Bei der Eingabe muss der **pfncallback** -Member dieser Struktur auf eine von der Anwendung definierte [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion verweisen.</span><span class="sxs-lookup"><span data-stu-id="569a3-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="569a3-134">Bei der Ausgabe kann der **dwError** -Member einen Fehlercode ungleich 0 (null) enthalten, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="569a3-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="569a3-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="569a3-135">Return value</span></span>

<span data-ttu-id="569a3-136">Diese Meldung gibt die Anzahl der gelesenen Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="569a3-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="569a3-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="569a3-137">Remarks</span></span>

<span data-ttu-id="569a3-138">Wenn Sie eine **EM- \_ StreamIn** -Nachricht senden, führt das Rich Edit-Steuerelement wiederholte Aufrufe an die [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion aus, die vom **pfncallback** -Member der [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="569a3-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="569a3-139">Jedes Mal, wenn die Rückruffunktion aufgerufen wird, füllt Sie einen Puffer mit Daten aus, die in das Steuerelement eingelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="569a3-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="569a3-140">Dies wird fortgesetzt, bis die Rückruffunktion anzeigt, dass der Stream-in-Vorgang abgeschlossen wurde oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="569a3-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="569a3-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="569a3-141">Requirements</span></span>



| <span data-ttu-id="569a3-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="569a3-142">Requirement</span></span> | <span data-ttu-id="569a3-143">Wert</span><span class="sxs-lookup"><span data-stu-id="569a3-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="569a3-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="569a3-144">Minimum supported client</span></span><br/> | <span data-ttu-id="569a3-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="569a3-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="569a3-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="569a3-146">Minimum supported server</span></span><br/> | <span data-ttu-id="569a3-147">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="569a3-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="569a3-148">Header</span><span class="sxs-lookup"><span data-stu-id="569a3-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="569a3-149"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="569a3-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="569a3-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="569a3-151">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="569a3-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="569a3-152">**Editstream**</span><span class="sxs-lookup"><span data-stu-id="569a3-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="569a3-153">*Editstreamcallback*</span><span class="sxs-lookup"><span data-stu-id="569a3-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="569a3-154">**EM- \_ StreamOut**</span><span class="sxs-lookup"><span data-stu-id="569a3-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





