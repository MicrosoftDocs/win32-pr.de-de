---
title: Sonstige Frameworkkonst constants (Msctf.h)
description: Verschiedene Frameworkkonst constants geben Einstellungen für Clients, Prozesse oder Text an.
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
ms.openlocfilehash: f9bcd6ad253e71d662cbc713398e65c6a250863e18a9fe2d461a2d93717fb7b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906010"
---
# <a name="miscellaneous-framework-constants"></a>Sonstige Frameworkkonst constants

Verschiedene Frameworkkonst constants geben Einstellungen für Clients, Prozesse oder Text an.



| Konstante/Wert                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**TF \_ CLIENTID \_ NULL**</dt> <dt>((TfClientId)0)</dt> </dl>                        | Gibt für einen Textdienst an, dass der Client deaktiviert ist. Weitere Informationen [finden Sie unter TfClientId](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**TF \_ UNGÜLTIGER \_ GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt> </dl>               | Der [TfGuidAtom-Wert](tfguidatom.md) für den aktuellen Prozess ist ungültig.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**TF \_ \_STANDARDAUSWAHL**</dt> <dt>( TS DEFAULT SELECTION \_ \_ )</dt> </dl> | Verwenden Sie die Standardauswahl. Wird von [ITfContext::GetSelection,](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)und [ITextStoreAnchor::GetSelection verwendet.](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**TF \_ GTP \_ INCL \_ TEXT**</dt> <dt>( 0x1 )</dt> </dl>                               | Gibt an, dass die [ITfEditRecord::GetTextAndPropertyUpdates-Methode](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) die Auflistung von Bereichsobjekten erhält, die den während der Bearbeitungssitzung geänderten Text abdecken.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**TF \_ HF \_ OBJECT**</dt> <dt>( 1 )</dt> </dl>                                              | Die Bereichsverschiebung wird beendet, wenn ein eingebettetes Objekt gefunden wird. Wird im **dwFlags-Member** der [TF \_ HALTCOND-Struktur](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) verwendet.<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**TF \_ \_IE-KORREKTUR**</dt> <dt>( 1 )</dt> </dl>                                  | Der Text ist eine Transformation (Korrektur) vorhandener Inhalte, sodass andere Textdienste daten beibehalten können, die dem ursprünglichen Text zugeordnet sind. Wird im *dwFlags-Parameter* von [ITfRange::InsertEmbedded verwendet.](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**TF \_ UNGÜLTIGES \_ COOKIE**</dt> <dt>( 0xffffffff )</dt> </dl>                      | Wird nicht verwendet.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**TF \_ UNGÜLTIGES \_ COOKIE \_ BEARBEITEN**</dt> <dt>( 0 )</dt> </dl>               | Wird nicht verwendet.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**TF \_ POPF \_ ALL**</dt> <dt>( 0x1 )</dt> </dl>                                               | Alle Kontexte werden aus dem Stapel entfernt. Wird im *dwFlags-Parameter* von [ITfDocumentMgr::P op verwendet.](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**TF \_ ST \_ CORRECTION**</dt> <dt>( 1 )</dt> </dl>                                  | Der Text ist eine Transformation (Korrektur) vorhandener Inhalte, sodass andere Textdienste daten beibehalten können, die dem ursprünglichen Text zugeordnet sind. Wird im *dwFlags-Parameter* von [ITfRange::SetText verwendet.](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**TF \_ \_TU-KORREKTUR**</dt> <dt>( 0x1 )</dt> </dl>                                | Die Textänderung ist das Ergebnis einer Transformation (Korrektur) vorhandener Inhalte. Dies bedeutet, dass sich die Semantik des Texts nicht geändert hat. Wird im *dwFlags-Parameter* von [ITfPropertyStore::OnTextUpdated verwendet.](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**TF \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt> </dl>                                | Wird nicht verwendet.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





