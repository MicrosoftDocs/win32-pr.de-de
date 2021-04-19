---
title: TF_ES_ Konstanten (msctf. h)
description: Die folgenden Konstanten werden von der ITF Context requesteditsession-Methode verwendet.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345918"
---
# <a name="tf_es_-constants"></a>TF \_ es- \_ \* Konstanten

Die folgenden Konstanten werden von der [ITF context:: requesteditsession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) -Methode verwendet.



| Konstante/Wert                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**Tf \_ ES \_ asyncdontcare**</dt> <dt>(0)</dt> </dl> | Die Bearbeitungs Sitzung kann nach dem Ermessen des Vorgesetzten synchron oder asynchron erfolgen. Der Manager versucht, eine synchrone Bearbeitungs Sitzung zu planen, um die Leistung zu verbessern. Dieser Wert kann nicht mit den TF \_ es- \_ Werten "Async" oder "TF \_ es Sync" kombiniert werden \_ .<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**Tf \_ ES \_ Sync**</dt> <dt>(0x1)</dt> </dl>                          | Die Bearbeitungs Sitzung muss synchron sein, oder die Anforderung schlägt fehl (mit tf \_ E \_ synchron). Dieses Flag sollte nur in dokumentierten Situationen verwendet werden (z. b. bei der Tastatureingabe), bei denen es erwartungsgemäß funktioniert. Andernfalls schlägt der-Vorgang wahrscheinlich fehl. Dieser Wert kann nicht mit den \_ Async-Werten von tf es \_ asyncdontcare oder TF es kombiniert werden \_ \_ .<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**Tf \_ \_Lese**</dt> Vorgänge <dt>(0x2)</dt> </dl>                          | Fordert schreibgeschützten Zugriff auf den Kontext an.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**Tf \_ ES- \_ Lesevorgang**</dt> <dt>(0x6)</dt> </dl>           | Fordert den Lese-/Schreibzugriff auf den Kontext an.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt> </dl>                       | Die Bearbeitungs Sitzung muss asynchron sein, oder die Anforderung kann nicht ausgeführt werden. Dieser Wert kann nicht mit den TF \_ es \_ asyncdontcare-oder TF \_ es- \_ Synchronisierungs Werten kombiniert werden.<br/>                                                                                                                                                                                         |



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

[ITF context:: requestedizession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





