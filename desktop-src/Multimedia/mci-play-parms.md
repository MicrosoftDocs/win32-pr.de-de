---
title: MCI_PLAY_PARMS-Struktur (mciapi. h)
description: Die MCI-Wiedergabe-Parametern- \_ \_ Struktur enthält Positionsinformationen für den MCI \_ Play-Befehl.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- MCI_PLAY_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949399"
---
# <a name="mci_play_parms-structure"></a>MCI-Wiedergabe-Parametern- \_ \_ Struktur

Die **MCI- \_ Wiedergabe- \_ Parametern** -Struktur enthält Positionsinformationen für den [**MCI \_ Play**](mci-play.md) -Befehl.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwfrom**
</dt> <dd>

Wiedergabe Position

</dd> <dt>

**dwto**
</dt> <dd>

Position der Wiedergabe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

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

[**MCI- \_ Play**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

