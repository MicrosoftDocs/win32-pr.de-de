---
title: TF_SD_ Konstanten (msctf. h)
description: Die TF \_ SD \_ \-Konstanten beschreiben den Dokument Status.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103014"
---
# <a name="tf_sd_-constants"></a>TF \_ SD- \_ \* Konstanten

Die TF \_ SD- \_ \* Konstanten beschreiben den Dokument Status.



| Konstante/Wert                                                                                                                                                                                                                              | BESCHREIBUNG                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**Tf \_ SD \_**</dt> schreibgeschützt <dt>(TS \_ SD \_</dt> schreibgeschützt) </dl> | Das Dokument ist schreibgeschützt und kann nicht geändert werden.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**Tf \_ SD- \_ Lade**</dt> Vorgänge <dt>(TS \_ SD- \_ Laden)</dt> </dl>     | Das Dokument wird geladen und kann unvollständig sein.<br/>    |



## <a name="remarks"></a>Bemerkungen

Der **dwdynamicflags** -Member der [tf- \_ Status](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) Struktur verwendet diese Konstanten.

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

[TF- \_ Status](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[TS \_ SD- \_ \* Konstanten](ts-sd--constants.md)
</dt> <dt>

[Itfcontextowner:: GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITF contextownerservices:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP:: GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITF statussunk:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

