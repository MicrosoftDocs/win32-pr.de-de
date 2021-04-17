---
title: Sonstige frameworkkonstanten (msctf. h)
description: Verschiedene frameworkkonstanten geben Einstellungen für Clients, Prozesse oder Text an.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478423"
---
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="ac701-103">Sonstige frameworkkonstanten</span><span class="sxs-lookup"><span data-stu-id="ac701-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="ac701-104">Verschiedene frameworkkonstanten geben Einstellungen für Clients, Prozesse oder Text an.</span><span class="sxs-lookup"><span data-stu-id="ac701-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="ac701-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="ac701-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="ac701-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac701-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="ac701-107"><dt>**Tf \_ ClientID \_ null**</dt> <dt>((tfclientid) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="ac701-108">Gibt einem Text Dienst an, dass der Client deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ac701-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="ac701-109">Siehe [tfclientid](tfclientid.md).</span><span class="sxs-lookup"><span data-stu-id="ac701-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="ac701-110"><dt>**Tf \_ Ungültiges \_ guidatom**</dt> <dt>((tfguidatom) 0)</dt> .</span><span class="sxs-lookup"><span data-stu-id="ac701-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="ac701-111">Der [tfguidatom](tfguidatom.md) -Wert für den aktuellen Prozess ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ac701-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="ac701-112"><dt>**Tf \_ Standard \_ Auswahl**</dt> <dt>(TS- \_ Standard \_ Auswahl)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="ac701-113">Verwenden Sie die Standardauswahl.</span><span class="sxs-lookup"><span data-stu-id="ac701-113">Use the default selection.</span></span> <span data-ttu-id="ac701-114">Wird von [ITF context:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)und [itextstoreanchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="ac701-115"><dt>**Tf \_ GTP \_ inkl \_ Text**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="ac701-116">Gibt an, dass die [itfeditrecord:: gettextandpropertyupdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) -Methode die Auflistung von Bereichs Objekten abruft, die den Text abdecken, der während der Bearbeitungs Sitzung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac701-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="ac701-117"><dt>**Tf \_ HF- \_ Objekt**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="ac701-118">Der Bereichs Wechsel wird beendet, wenn ein eingebettetes Objekt gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="ac701-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="ac701-119">Wird im **dwFlags** -Member der [tf \_ -"Hald"-](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="ac701-120"><dt>**Tf \_ IE- \_ Korrektur**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="ac701-121">Bei dem Text handelt es sich um eine Transformation (Korrektur) vorhandener Inhalte, sodass andere Text Dienste die dem ursprünglichen Text zugeordneten Daten beibehalten können.</span><span class="sxs-lookup"><span data-stu-id="ac701-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="ac701-122">Wird im *dwFlags* -Parameter von [itfrange:: insertembedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="ac701-123"><dt>**Tf \_ Ungültiges \_ Cookie**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="ac701-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="ac701-125"><dt>**Tf \_ Ungültiges \_ Bearbeitungs \_ Cookie**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="ac701-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="ac701-127"><dt>**Tf \_ Popf \_ alle**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="ac701-128">Alle Kontexte werden aus dem Stapel entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac701-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="ac701-129">Wird im *dwFlags* -Parameter von [ITF documentmgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="ac701-130"><dt>**Tf \_ St- \_ Korrektur**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="ac701-131">Bei dem Text handelt es sich um eine Transformation (Korrektur) vorhandener Inhalte, sodass andere Text Dienste die dem ursprünglichen Text zugeordneten Daten beibehalten können.</span><span class="sxs-lookup"><span data-stu-id="ac701-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="ac701-132">Wird im *dwFlags* -Parameter von [itfrange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="ac701-133"><dt>**Tf \_ TU- \_ Korrektur**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="ac701-134">Die Textänderung ist das Ergebnis einer Transformation (Korrektur) vorhandener Inhalte.</span><span class="sxs-lookup"><span data-stu-id="ac701-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="ac701-135">Dies impliziert, dass die Semantik des Texts nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac701-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="ac701-136">Wird im *dwFlags* -Parameter von [itbpropertystore:: ontextupexpverwendet](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span><span class="sxs-lookup"><span data-stu-id="ac701-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="ac701-137"><dt>**Tf \_ US \_ hidetipui**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="ac701-138">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac701-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="ac701-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac701-139">Requirements</span></span>



| <span data-ttu-id="ac701-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac701-140">Requirement</span></span> | <span data-ttu-id="ac701-141">Wert</span><span class="sxs-lookup"><span data-stu-id="ac701-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac701-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac701-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ac701-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac701-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ac701-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac701-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ac701-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac701-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ac701-146">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ac701-146">Redistributable</span></span><br/>          | <span data-ttu-id="ac701-147">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac701-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="ac701-148">Header</span><span class="sxs-lookup"><span data-stu-id="ac701-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac701-149"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac701-150">IDL</span><span class="sxs-lookup"><span data-stu-id="ac701-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac701-151"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac701-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac701-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac701-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac701-153">ITextStoreACP:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="ac701-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="ac701-154">Itextstoreanchor:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="ac701-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="ac701-155">ITF context:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="ac701-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="ac701-156">ITF documentmgr::P op</span><span class="sxs-lookup"><span data-stu-id="ac701-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="ac701-157">Itfeditrecord:: gettextandpropertyupdates</span><span class="sxs-lookup"><span data-stu-id="ac701-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="ac701-158">Itmapropertystore:: ontextupexp</span><span class="sxs-lookup"><span data-stu-id="ac701-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="ac701-159">Itfrange:: insertembedded</span><span class="sxs-lookup"><span data-stu-id="ac701-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="ac701-160">Itfrange:: SetText</span><span class="sxs-lookup"><span data-stu-id="ac701-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="ac701-161">Tfclientid</span><span class="sxs-lookup"><span data-stu-id="ac701-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="ac701-162">Tfguidatom</span><span class="sxs-lookup"><span data-stu-id="ac701-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="ac701-163">TF \_ -Halt-ID</span><span class="sxs-lookup"><span data-stu-id="ac701-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





