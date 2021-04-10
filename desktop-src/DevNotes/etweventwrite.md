---
description: 'Weitere Informationen zu: etweventwrite-Funktion'
title: Etweventwrite
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
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041480"
---
# <a name="etweventwrite-function"></a>Etweventwrite-Funktion

[Die etweventwrite-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.]

Schreibt ein Basisereignis in eine Sitzung.

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

*Reghandle*
</dt> <dd>

Reghandle für den Anbieter.

</dd> <dt>

*EventDescriptor*
</dt> <dd>

Der Ereignis Deskriptor des Ereignisses, das protokolliert werden soll.

</dd> <dt>

*Userdatacount*
</dt> <dd>

Anzahl von Benutzerdaten Elementen.

</dd> <dt>

*UserData*
</dt> <dd>

Zeiger auf ein Array von Benutzerdaten Elementen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Win32-Fehlercode.


## <a name="remarks"></a>Bemerkungen

Die etweventwrite-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden.

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
