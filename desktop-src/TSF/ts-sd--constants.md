---
title: TS_SD_ Konstanten (textstor. h)
description: Die TS \_ SD \_ \-Konstanten beschreiben dynamische Dokument Zustände, die von einer Anwendung zur Laufzeit verwendet werden.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337918"
---
# <a name="ts_sd_-constants"></a>TS \_ SD- \_ \* Konstanten

Die TS \_ SD- \_ \* Konstanten beschreiben dynamische Dokument Zustände, die von einer Anwendung zur Laufzeit verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                                              | BESCHREIBUNG                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**TS \_ SD \_**</dt> schreibgeschützt <dt>(0x1)</dt> </dl>                              | Das Dokument ist schreibgeschützt und kann nicht geändert werden.<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**TS \_ SD- \_ Lade**</dt> Vorgänge <dt>(0x2)</dt> </dl>                                 | Das Dokument wird geladen und ist möglicherweise unvollständig.<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**TS \_ SD \_ maskall**</dt> <dt>(TS \_ SD Schreib geschützter \_ \| TS \_ SD- \_ Ladevorgang)</dt> </dl> | Das Dokument ist schreibgeschützt und wird geladen.<br/>       |



## <a name="remarks"></a>Bemerkungen

Der **dwdynamicflags** -Member der [TS- \_ Status](/windows/desktop/api/Textstor/ns-textstor-ts_status) Struktur verwendet diese Konstanten.

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

[TS- \_ Status](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[TF \_ SD- \_ \* Konstanten](tf-sd--constants.md)
</dt> </dl>

 

 





