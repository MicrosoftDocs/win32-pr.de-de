---
title: TS_ATTR_ Konstanten (textstor. h)
description: Die TS \_ attr \_ \-Konstanten werden verwendet, um die Werte von Dokument Attributen abzurufen und zu ändern. Diese Konstanten bilden mögliche Werte von Bitfeld-Flags in ITextStoreACP-und itextstoreanchor-Methoden.
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477997"
---
# <a name="ts_attr_-constants"></a>TS \_ attr- \_ \* Konstanten

Die TS \_ attr \_ \* -Konstanten werden verwendet, um die Werte von Dokument Attributen abzurufen und zu ändern. Diese Konstanten bilden mögliche Werte von Bitfeld-Flags in [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) und [itextstoreanchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) -Methoden.



| Konstante/Wert                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ Attr \_ \_ rückwärts suchen**</dt> <dt>(0x1)</dt> </dl>        | Suchen Sie rückwärts von der Start-oder Ankerposition an der Position, an der ein Übergang in einem Dokument Attribut Wert auftritt. Der Standardwert ist Search Forward.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ Attr- \_ Suche nach \_ gewünschten \_ Offset**</dt> <dt>(0x2)</dt> </dl> | Gibt die Anzahl der Zeichen zwischen dem Startzeichen oder der Ankerposition (**acpstart** in [ITextStoreACP:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) oder **pastart** in [itextstoreanchor:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) und der Position an, an der ein Attribut Übergang auftritt.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ Attr \_ Find \_ Updatestart**</dt> <dt>(0x4)</dt> </dl>  | Wird von [itextstoreanchor:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) verwendet, um den Eingabe Anker beim nächsten Attribut Übergang (sofern gefunden) zu positionieren. Andernfalls wird der Eingabe Anker nicht geändert.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ Attr \_ \_ \_ Suchwert suchen**</dt> <dt>(0x8)</dt> </dl>    | Laden unterstützter Dokument Attributwerte in die [TS \_ attrval](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) -Struktur.<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ Attr \_ Find \_ will \_ End**</dt> <dt>(0x10)</dt> </dl>         | Wird von [ITextStoreACP:: requestatus trstransitioningatposition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) und [itextstoreanchor:: requestatus trstransitioningatposition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) verwendet, um die Dokument Attributwerte abzurufen, die an der angegebenen Zeichenposition oder Ankerposition enden.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ Attr- \_ Suche \_ ausgeblendet**</dt> <dt>(0x20)</dt> </dl>                | Reserviert.<br/>                                                                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TS \_ -attrd](ts-attrid.md)
</dt> <dt>

[TS- \_ attrval](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP:: requestatus-stransitioningatposition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[Itextstoreanchor:: findnextattrtransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[Itextstoreanchor:: requestatus-stransitioningatposition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





