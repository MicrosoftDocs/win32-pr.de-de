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
# <a name="miscellaneous-framework-constants"></a>Sonstige frameworkkonstanten

Verschiedene frameworkkonstanten geben Einstellungen für Clients, Prozesse oder Text an.



| Konstante/Wert                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**Tf \_ ClientID \_ null**</dt> <dt>((tfclientid) 0)</dt> </dl>                        | Gibt einem Text Dienst an, dass der Client deaktiviert ist. Siehe [tfclientid](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**Tf \_ Ungültiges \_ guidatom**</dt> <dt>((tfguidatom) 0)</dt> . </dl>               | Der [tfguidatom](tfguidatom.md) -Wert für den aktuellen Prozess ist ungültig.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**Tf \_ Standard \_ Auswahl**</dt> <dt>(TS- \_ Standard \_ Auswahl)</dt> </dl> | Verwenden Sie die Standardauswahl. Wird von [ITF context:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)und [itextstoreanchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)verwendet.<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**Tf \_ GTP \_ inkl \_ Text**</dt> <dt>(0x1)</dt> </dl>                               | Gibt an, dass die [itfeditrecord:: gettextandpropertyupdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) -Methode die Auflistung von Bereichs Objekten abruft, die den Text abdecken, der während der Bearbeitungs Sitzung geändert wurde.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**Tf \_ HF- \_ Objekt**</dt> <dt>(1)</dt> </dl>                                              | Der Bereichs Wechsel wird beendet, wenn ein eingebettetes Objekt gefunden wird. Wird im **dwFlags** -Member der [tf \_ -"Hald"-](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) Struktur verwendet.<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**Tf \_ IE- \_ Korrektur**</dt> <dt>(1)</dt> </dl>                                  | Bei dem Text handelt es sich um eine Transformation (Korrektur) vorhandener Inhalte, sodass andere Text Dienste die dem ursprünglichen Text zugeordneten Daten beibehalten können. Wird im *dwFlags* -Parameter von [itfrange:: insertembedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)verwendet.<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**Tf \_ Ungültiges \_ Cookie**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                      | Nicht verwendet.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**Tf \_ Ungültiges \_ Bearbeitungs \_ Cookie**</dt> <dt>(0)</dt> </dl>               | Nicht verwendet.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**Tf \_ Popf \_ alle**</dt> <dt>(0x1)</dt> </dl>                                               | Alle Kontexte werden aus dem Stapel entfernt. Wird im *dwFlags* -Parameter von [ITF documentmgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)verwendet.<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**Tf \_ St- \_ Korrektur**</dt> <dt>(1)</dt> </dl>                                  | Bei dem Text handelt es sich um eine Transformation (Korrektur) vorhandener Inhalte, sodass andere Text Dienste die dem ursprünglichen Text zugeordneten Daten beibehalten können. Wird im *dwFlags* -Parameter von [itfrange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)verwendet.<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**Tf \_ TU- \_ Korrektur**</dt> <dt>(0x1)</dt> </dl>                                | Die Textänderung ist das Ergebnis einer Transformation (Korrektur) vorhandener Inhalte. Dies impliziert, dass die Semantik des Texts nicht geändert wurde. Wird im *dwFlags* -Parameter von [itbpropertystore:: ontextupexpverwendet](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**Tf \_ US \_ hidetipui**</dt> <dt>0x00000001</dt> </dl>                                | Nicht verwendet.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[Itextstoreanchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITF context:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITF documentmgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[Itfeditrecord:: gettextandpropertyupdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[Itmapropertystore:: ontextupexp](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[Itfrange:: insertembedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[Itfrange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Tfclientid](tfclientid.md)
</dt> <dt>

[Tfguidatom](tfguidatom.md)
</dt> <dt>

[TF \_ -Halt-ID](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





