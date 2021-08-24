---
title: MCI_VD_PLAY_PARMS -Struktur (Mciapi.h)
description: Die MCI VD PLAY PARMS-Struktur enthält Positions- und Geschwindigkeitsinformationen für den \_ \_ \_ MCI \_ PLAY-Befehl für videodisc-Geräte.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c2aef6915d1e3cc325d5b9f8e1c7fe176a878c2d84080b5f8a77eaf034afc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783865"
---
# <a name="mci_vd_play_parms-structure"></a>MCI \_ VD \_ PLAY \_ PARMS-Struktur

Die **MCI \_ VD \_ PLAY \_ PARMS-Struktur** enthält Positions- und Geschwindigkeitsinformationen für den [**MCI \_ PLAY-Befehl**](mci-play.md) für videodisc-Geräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position, von der aus sie abspielt werden soll.

</dd> <dt>

**dwTo**
</dt> <dd>

Position, an der abspielt werden soll.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Wiedergabegeschwindigkeit in Frames pro Sekunde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

Sie können die [**MCI \_ PLAY \_ PARMS-Struktur**](mci-play-parms.md) anstelle von **MCI \_ VD \_ PLAY \_ PARMS** verwenden, wenn Sie die erweiterten Datenmitglieder nicht verwenden.

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

[**MCI \_ PLAY \_ PARMS**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

