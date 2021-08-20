---
description: 'Weitere Informationen zu: EtwEventWrite-Funktion'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: b8e06c2a0922038e37766f44c0b9fcd7c85bbb7fd4fa4bd0841192be9e4e9087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162101"
---
# <a name="etweventwrite-function"></a>EtwEventWrite-Funktion

[Die EtwEventWrite-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.]

Schreibt ein einfaches Ereignis in eine Sitzung.

## <a name="syntax"></a>Syntax

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
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

*UserDataCount*
</dt> <dd>

Anzahl der Benutzerdatenelemente.

</dd> <dt>

*UserData*
</dt> <dd>

Zeiger auf ein Array von Benutzerdatenelementen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Win32-Fehlercode.


## <a name="remarks"></a>Hinweise

Die EtwEventWrite-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden.

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
