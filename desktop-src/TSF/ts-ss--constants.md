---
title: TS_SS_ Konstanten (textstor. h)
description: Die TS \_ SS \_ \-Konstanten, die vor der Laufzeit in der TS- \_ Status Struktur definiert werden, beschreiben statische Dokument Zustände.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337290"
---
# <a name="ts_ss_-constants"></a>TS- \_ SS- \_ \* Konstanten

Die TS- \_ SS- \_ \* Konstanten, die vor der Laufzeit in der [**TS- \_ Status**](/windows/desktop/api/Textstor/ns-textstor-ts_status) Struktur definiert werden, beschreiben statische Dokument Zustände.



| Konstante/Wert                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**TS \_ SS- \_ disjointsel**</dt> <dt>(0x1)</dt> </dl>                             | Das Dokument unterstützt mehrere Auswahlmöglichkeiten.<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**TS \_ SS- \_ Regionen**</dt> <dt>(0x2)</dt> </dl>                                         | Das Dokument kann mehrere Regionen enthalten.<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**TS \_ SS \_ Transitory**</dt> <dt>(0x4)</dt> </dl>                                | Es wird erwartet, dass das Dokument einen kurzen Verwendungs Zeitraum hat.<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**TS \_ SS \_ nohiddentext**</dt> <dt>(0x8)</dt> </dl>                          | Das Dokument enthält niemals ausgeblendeten Text.<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**TS \_ SS \_ tkbautkorrigitenable**</dt> <dt>(0x10)</dt> </dl> | **Beginnend mit Windows 8:** Das Dokument unterstützt die von der Touchscreen-Tastatur bereitgestellte automatische Korrektur.<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**TS \_ SS \_ tkbvorhertionenable**</dt> <dt>(0x20)</dt> </dl>    | **Beginnend mit Windows 8:** Das Dokument unterstützt Text Vorschläge von der Touchscreen-Tastatur.<br/> |



## <a name="remarks"></a>Bemerkungen

Der **dwstaticflags** -Member der **TS- \_ Status** Struktur verwendet diese Konstanten.

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

[**TS- \_ Status**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**TF- \_ Status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

