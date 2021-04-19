---
title: TS_AS_ Konstanten (textstor. h)
description: Die folgenden Flags geben die Ereignisse an, die die AdviseSink-Methoden aufzurufen.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346322"
---
# <a name="ts_as_-constants"></a>TS \_ als \_ \* Konstanten

Die folgenden Flags geben die Ereignisse an, die die **AdviseSink** -Methoden aufzurufen.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_ Als \_ Text \_ Änderung**</dt> <dt>(0x1)</dt> </dl>                                                                                                               | Der Text wird im Dokument geändert.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_ AS \_ - \_ Änderung**</dt> <dt>(0x2)</dt> </dl>                                                                                                                  | Im Dokument ist Text ausgewählt.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_ Bei \_ \_ Änderung des Layouts**</dt> <dt>(0x4)</dt> </dl>                                                                                                         | Das Layout des Dokuments wird geändert.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ Als \_ attr- \_ Änderung**</dt> <dt>(0x8)</dt> </dl>                                                                                                               | Die Attribute des Dokuments werden geändert.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_ Als \_ Status \_ Änderung**</dt> <dt>(0x10)</dt> </dl>                                                                                                        | Der Status des Dokuments wird geändert.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_ \_alle \_ senken**</dt> <dt>(TS \_ As Text Change TS as \_ \_ \| \_ \_ SEL \_ Change TS as Layout Change TS as \| \_ \_ \_ \| \_ \_ attr Change TS as \_ \| \_ \_ Status \_ Change)</dt> </dl> | Eines der vorherigen vier Ereignisse ist im Dokument aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





