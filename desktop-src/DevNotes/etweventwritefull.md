---
description: Schreibt ein vollständiges Ereignis in eine Sitzung.
title: EtwEventWriteFull
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
ms.openlocfilehash: 1fd25931e6a58b97e052ecd7da43bd651688d2bf726d8b5ba2acd84ce820be7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653429"
---
# <a name="etweventwritefull-function"></a>EtwEventWriteFull-Funktion

[Die EtwEventWriteFull-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.]

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

*RegHandle*
</dt> <dd>

RegHandle für den Anbieter.

</dd> <dt>

*Eventdescriptor* 
</dt> <dd>

Ereignisdeskriptor des zu protokollierende Ereignisses.

</dd> <dt>

*EventProperty*
</dt> <dd>

Vom Benutzer angegebenes Flag.

</dd> <dt>

*ActivityId*
</dt> <dd>

Aktivitäts-ID.

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

Zugehörige Aktivitäts-ID.

</dd> <dt>

*UserDataCount*
</dt> <dd>

Die Anzahl der Benutzerdatenelemente.

</dd> <dt>

*UserData*
</dt> <dd>

Zeiger auf ein Array von Benutzerdatenelementen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Win32-Fehlercode.

## <a name="remarks"></a>Hinweise

Die EtwEventWriteFull-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden.


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | ntetw.h |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
