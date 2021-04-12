---
description: Definiert Methoden, die die iTablet-Schnittstellen Ereignisse verarbeiten.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Itableteventsink-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218367"
---
# <a name="itableteventsink-interface"></a>Itableteventsink-Schnittstelle

Definiert Methoden, die die [**iTablet-Schnittstellen**](itablet.md) Ereignisse verarbeiten.

## <a name="members"></a>Member

Die **itableteventsink** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itableteventsink** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itableteventsink** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Contextcreate**](itableteventsink-contextcreate.md)       | Tritt auf, wenn ein neuer Tablet-Kontext erstellt wird.<br/>                                          |
| [**Contextdestroy**](itableteventsink-contextdestroy.md)     | Tritt auf, wenn ein Tablet-Kontext zerstört wird.<br/>                                      |
| [**Cursor**](itableteventsink-cursordown.md)             | Tritt auf, wenn der tablettstifttipp die digitalisierende Tablet-Oberfläche kontaktiert.<br/>                    |
| [**Cursor Bereich**](itableteventsink-cursorinrange.md)       | Tritt auf, wenn ein Tablettstift in den Bereich der Erkennung des Digitalisierungsprogramms kommt.<br/>                 |
| [**Cursor verschieben**](itableteventsink-cursormove.md)             | Tritt auf, wenn der Cursor über den Tablet-Digitalisierer bewegt wird.<br/>                               |
| [**Currsornew**](itableteventsink-cursornew.md)               | Tritt auf, wenn dem System ein neuer Tablettstift hinzugefügt wird.<br/>                                      |
| [**Cursor-Ausgabe**](itableteventsink-cursoroutofrange.md) | Tritt auf, wenn der Tablettstift den physischen Erkennungsbereich (Nähe) des Tablets verlässt.<br/> |
| [**Cursor**](itableteventsink-cursorup.md)                 | Tritt auf, wenn der Benutzer den Tablettstift von der tabletdigitalisiereroberfläche ausgelöst hat.<br/>         |
| [**Pakete**](itableteventsink-packets.md)                   | Tritt auf, wenn sich der Tablettstift auf dem Digitalisierer bewegt.<br/>                                    |
| [**System Event**](itableteventsink-systemevent.md)           | Tritt auf, wenn ein System Ereignis verfügbar ist.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code zeigt, wie die **itableteventsink** -Schnittstelle definiert wird.

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

