---
title: MCI_STATUS_PARMS-Struktur (mciapi. h)
description: Die Struktur des MCI- \_ Status \_ Parametern enthält Informationen zum MCI- \_ Status Befehl.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949533"
---
# <a name="mci_status_parms-structure"></a>Struktur von MCI- \_ Status- \_ Parametern

Die Struktur des **MCI- \_ Status \_ Parametern** enthält Informationen zum [**MCI- \_ Status**](mci-status.md) Befehl.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwreturn**
</dt> <dd>

Enthält Informationen zur Rückgabe.

</dd> <dt>

**dwitem**
</dt> <dd>

Die Funktion, die abgefragt wird.

</dd> <dt>

**dwtrack**
</dt> <dd>

Länge oder Anzahl der Spuren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das MCI \_ - \_ statuselementflag muss im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion festgelegt werden, um das **dwitem** -Element zu validieren, das eine der Konstanten enthalten muss, die angeben, welche Status Informationen angefordert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI- \_ Status**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

