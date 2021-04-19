---
title: TF_IAS_ Konstanten (msctf. h)
description: Die TF \_ IAS \_ \ Konstanten werden in Methoden verwendet, die Text oder eingebettete Objekte an einer Auswahl-oder Einfügemarke einfügen.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339151"
---
# <a name="tf_ias_-constants"></a>TF \_ IAS- \_ \* Konstanten

Die TF \_ IAS- \_ \* Konstanten werden als bitfeldflags in Methoden verwendet, die Text oder eingebettete Objekte an einer Auswahl-oder Einfügemarke einfügen.



| Konstante/Wert                                                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <dt>**Tf \_ IAS \_ noquery**</dt> <dt>(0x1)</dt> </dl>                                                       | Der Text wird eingefügt, und der Bereichs Zeiger wird beim Beenden auf **null** festgelegt. Kann nicht mit dem TF \_ IAS- \_ Flag queryonly kombiniert werden.<br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <dt>**Tf \_ IAS- \_ queryonly**</dt> <dt>(0x2)</dt> </dl>                                                 | Führen Sie den Einfügevorgang nicht aus. Für den Aufrufer muss nur der Bereichs Zeiger festgelegt werden. Kann nicht mit dem TF \_ IAS \_ noquery-Flag kombiniert werden.<br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <dt>**Tf \_ IAS \_ keine \_ Standard \_ Komposition**</dt> <dt>(0x80000000)</dt> </dl> | TSF erstellt keine Standard Komposition, wenn eine Komposition erforderlich ist. Der Aufrufer muss eine Komposition für den Bereich starten.<br/>         |



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

[ITextStoreACP:: insertembedentdatselection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[ITextStoreACP:: inserttextatselection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[Itextstoreanchor:: insertembedentdatselection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[Itextstoreanchor:: inserttextatselection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[Itfinsertatselection:: insertembedentdatselection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[Itfinsertatselection:: inserttextatselection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





