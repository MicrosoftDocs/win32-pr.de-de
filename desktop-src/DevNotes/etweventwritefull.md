---
description: Schreibt ein vollständiges Ereignis in eine Sitzung.
title: Etweventschreitefull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958491"
---
# <a name="etweventwritefull-function"></a>Etweventschreitefull-Funktion

[Die etweventwrite tefull-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.]

Schreibt ein vollständiges Ereignis in eine Sitzung.

## <a name="syntax"></a>Syntax

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Reghandle*
</dt> <dd>

Reghandle für den Anbieter.

</dd> <dt>

*EventDescriptor* 
</dt> <dd>

Der Ereignis Deskriptor des Ereignisses, das protokolliert werden soll.

</dd> <dt>

*EventProperty*
</dt> <dd>

Das Flag, das vom Benutzer angegeben wird.

</dd> <dt>

*ActivityId*
</dt> <dd>

Aktivitäts-ID.

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

Zugehörige Aktivitäts-ID.

</dd> <dt>

*Userdatacount*
</dt> <dd>

Die Anzahl der Benutzerdaten Elemente.

</dd> <dt>

*UserData*
</dt> <dd>

Zeiger auf ein Array von Benutzerdaten Elementen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Win32-Fehlercode.

## <a name="remarks"></a>Bemerkungen

Die etweventwrite tefull-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden.


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | ntetw. h |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWrite-Ex](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
