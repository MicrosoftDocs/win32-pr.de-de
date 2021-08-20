---
title: MCI_PLAY_PARMS-Struktur (Mciapi.h)
description: Die MCI \_ PLAY \_ PARMS-Struktur enthält Positionierungsinformationen für den MCI \_ PLAY-Befehl.
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
ms.openlocfilehash: 7bd45269cd74d15d2326bf4c6528d5778ef7a5a35e40dfd2a74134afafdbcb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803471"
---
# <a name="mci_play_parms-structure"></a>MCI \_ PLAY \_ PARMS-Struktur

Die **MCI \_ PLAY \_ PARMS-Struktur** enthält Positionierungsinformationen für den [**MCI \_ PLAY-Befehl.**](mci-play.md)

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

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position, aus der wiedergegeben werden soll.

</dd> <dt>

**dwTo**
</dt> <dd>

Position, an der wiedergegeben werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

