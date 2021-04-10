---
title: TF_SS_ Konstanten (msctf. h)
description: Die TF \_ SS \_ \-Konstanten, die vor der Laufzeit in der TF- \_ Status Struktur definiert werden, beschreiben statische Dokument Zustände.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040712"
---
# <a name="tf_ss_-constants"></a>TF \_ SS- \_ \* Konstanten

Die TF \_ SS- \_ \* Konstanten, die vor der Laufzeit in der [**tf- \_ Status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) Struktur definiert werden, beschreiben statische Dokument Zustände.



| Konstante/Wert                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**Tf \_ SS- \_ disjointsel**</dt> <dt>(TS \_ SS \_ disjointsel)</dt> </dl>                                     | Das Dokument unterstützt mehrere Auswahlmöglichkeiten.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**Tf \_ SS- \_ Regionen**</dt> <dt>(TS \_ SS- \_ Regionen)</dt> </dl>                                                     | Das Dokument kann mehrere Regionen enthalten.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**Tf \_ SS \_ Transitory**</dt> <dt>(TS \_ SS \_ Transitory)</dt> </dl>                                         | Es wird erwartet, dass das Dokument einen kurzen Verwendungs Zeitraum hat.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**Tf \_ SS \_ tkbautkorrigitenable**</dt> <dt>(TS \_ SS \_ tkbauttable)</dt> </dl> | **Beginnend mit Windows 8:** Das Dokument unterstützt die von der Touchscreen-Tastatur bereitgestellte automatische Korrektur.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**Tf \_ SS \_ tkbvorhertionenable**</dt> <dt>(TS \_ SS \_ tkbvorhertionenable)</dt> </dl>     | **Beginnend mit Windows 8:** Das Dokument unterstützt Text Vorschläge von der Touchscreen-Tastatur.<br/> |



## <a name="remarks"></a>Bemerkungen

Der **dwstaticflags** -Member der TF- \_ Status Struktur verwendet diese Konstanten.

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

[**TF- \_ Status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

