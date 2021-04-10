---
title: MCI_VD_PLAY_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI-" \_ \_ Play-Parser" \_ enthält Positions-und Geschwindigkeitsinformationen für den MCI- \_ Wiedergabe Befehl für Videodisk-Geräte.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS Struktur Windows Multimedia
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
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040650"
---
# <a name="mci_vd_play_parms-structure"></a>MCI-VD-Wiedergabe-Parametern- \_ \_ \_ Struktur

Die Struktur der **MCI-" \_ Play- \_ \_ Parser** " enthält Positions-und Geschwindigkeitsinformationen für den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl für Videodisk-Geräte.

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

</dd> <dt>

**dwspeed**
</dt> <dd>

Wiedergabegeschwindigkeit in Frames pro Sekunde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

Wenn Sie die erweiterten Datenmember nicht verwenden, können Sie die [**MCI- \_ Wiedergabe- \_ Parametern**](mci-play-parms.md) anstelle von **MCI- \_ VD-Play- \_ \_ para** Metern verwenden.

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

[**MCI- \_ Wiedergabe- \_ Parser**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

