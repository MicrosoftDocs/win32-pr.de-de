---
title: TS_SHIFT_ Konstanten (textstor. h)
description: Die TS \_ Shift \_ \-Konstanten werden von der ianchor-Schnittstelle für die Bearbeitung von ausgeblendetem Text und der Zeichen Zählung verwendet.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391930"
---
# <a name="ts_shift_-constants"></a>TS- \_ Verschiebungs \_ \* Konstanten

Die TS \_ -Verschiebungs \_ \* Konstanten werden von der **ianchor** -Schnittstelle zur Bearbeitung von ausgeblendetem Text und der Zeichen Zählung verwendet.



| Konstante/Wert                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**TS \_ UMSCHALT \_ Anzahl \_ ausgeblendet**</dt> <dt>(0x1)</dt> </dl> | Gibt an, dass der Anker an die nächste Bereichs Grenze verschoben wird, einschließlich der Grenze eines ausgeblendeten Text Bereichs. Wenn nicht festgelegt, wird der Anker nach einem beliebigen angrenzenden ausgeblendeten Text verschoben, bis ein Bereich von sichtbarem Text gefunden wird.<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**TS \_ UMSCHALT \_ Stopp \_ ausgeblendet**</dt> <dt>(0x2)</dt> </dl>    | Nicht verwendet.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**TS \_ UMSCHALT \_ Stopp \_ sichtbar**</dt> <dt>(0x4)</dt> </dl> | Nicht verwendet.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**TS \_ \_ \_ Nur Verschiebungs Anzahl**</dt> <dt>(0x8)</dt> </dl>       | Der Anker wird nicht verschoben.<br/>                                                                                                                                                                                                           |



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

[Ianchor:: Shif tregion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





