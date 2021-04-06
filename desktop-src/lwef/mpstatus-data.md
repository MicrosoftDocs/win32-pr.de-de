---
title: MPSTATUS_DATA Struktur (mpclient. h)
description: Enthält Daten über den aktuellen Status einer Komponente des Produkts.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSTATUS_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742304"
---
# <a name="mpstatus_data-structure"></a>Mpstatus- \_ Datenstruktur

Enthält Daten über den aktuellen Status einer Komponente des Produkts.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ComponentID**
</dt> <dd>

Typ: **[ **mpcomponent- \_ ID**](mpcomponent-id.md)**

</dd> <dd>

Bestimmte Komponenten-ID, für die der Status gemeldet wird.

</dd> <dt>

**fenckbar**
</dt> <dd>

Typ: **bool**

</dd> <dd>

Der für die Komponente angeforderte Status. **HRESULT** in den Rückruf Daten bedeutet, dass die Anforderung erfolgreich war oder fehlgeschlagen ist.

</dd> <dt>

**Componentstatus**
</dt> <dd>

Zusätzliche Statusdaten, abhängig vom Wert von " **ComponentID**".

> [!Note]  
> Führt derzeit zu einem Zeiger auf eine dummystruktur für alle möglichen Werte von " **ComponentID**".

 

<dl> <dt>

**Parkplatz**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Bei **ComponentID**  ==  **mpcomponent \_ als \_ Signatur**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**P2**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ AV- \_ Signatur**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**P3**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Beim Überwachen von " **ComponentID**  ==  **mpcomponent \_ Realtime \_**". Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**P4**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ OnAccess \_ Protection**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**betragen**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ ioav- \_ Schutz**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**verständigt**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn das Verhalten der **ComponentID-**  ==  **mpcomponent- \_ \_ Überwachung** erfolgt. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**P7**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Beim automatischen Scannen von **ComponentID**  ==  **\_ \_ mpcomponent**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**übrig**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ automatisch \_ sigupdate**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**P9**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ IPC**. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**pa**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ NIS** ist. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> <dt>

**PB**
</dt> <dd>

Typ: **pmpstatus \_ dataex nicht \_ verwendet**

</dd> <dd>

Wenn **ComponentID**  ==  **mpcomponent \_ Elam** ist. Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpcomponent- \_ ID**](mpcomponent-id.md)
</dt> <dt>

[**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





