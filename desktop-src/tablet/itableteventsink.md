---
description: Definiert Methoden, die die ITablet-Schnittstellenereignisse behandeln.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: ITabletEventSink-Schnittstelle
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
ms.openlocfilehash: a1a773f7b4e08a718c419de2d51c0ff3bd9bba551267188b12889b9ec99d4ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716459"
---
# <a name="itableteventsink-interface"></a>ITabletEventSink-Schnittstelle

Definiert Methoden, die die [**ITablet-Schnittstellenereignisse**](itablet.md) behandeln.

## <a name="members"></a>Member

Die **ITabletEventSink-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletEventSink verfügt** auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITabletEventSink-Schnittstelle** verfügt über diese Methoden.



| Methode                                                        | Beschreibung                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Tritt ein, wenn ein neuer Tablet-Kontext erstellt wird.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Tritt ein, wenn ein Tablet-Kontext zerstört wird.<br/>                                      |
| [**Cursordown**](itableteventsink-cursordown.md)             | Tritt ein, wenn die Tablettstiftspitze mit der Digitalisierungsoberfläche des Tablettstifts in Kontakt tritt.<br/>                    |
| [**Cursorinrange**](itableteventsink-cursorinrange.md)       | Tritt ein, wenn ein Stift innerhalb des Erkennungsbereichs des Digitizers liegt.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Tritt ein, wenn der Cursor über den Tablettdiger bewegt wird.<br/>                               |
| [**CursorNeu**](itableteventsink-cursornew.md)               | Tritt ein, wenn dem System ein neuer Stift hinzugefügt wird.<br/>                                      |
| [**Cursoroutofrange**](itableteventsink-cursoroutofrange.md) | Tritt ein, wenn der Tablettstift den physischen Erkennungsbereich (Nähe) des Tablets verlässt.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Tritt ein, wenn der Benutzer den Tablettstift von der Tablettdigisiereroberfläche ausgelöst hat.<br/>         |
| [**Pakete**](itableteventsink-packets.md)                   | Tritt ein, wenn sich der Stift auf dem Digitizer bewegt.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Tritt ein, wenn ein Systemereignis verfügbar ist.<br/>                                              |



 

## <a name="remarks"></a>Hinweise

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code zeigt, wie die **ITabletEventSink-Schnittstelle** definiert ist.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

