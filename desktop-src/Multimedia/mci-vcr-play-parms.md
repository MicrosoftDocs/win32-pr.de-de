---
title: MCI_VCR_PLAY_PARMS Struktur (VCR. h)
description: Die MCI- \_ VCR- \_ Wiedergabe \_ Parameter Struktur enthält Parameter für den MCI \_ -Wiedergabe Befehl für Video-Kassetten-Recorder.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956576"
---
# <a name="mci_vcr_play_parms-structure"></a>MCI \_ VCR-Wiedergabe-Parametern- \_ \_ Struktur

Die **MCI- \_ VCR- \_ Wiedergabe \_** Parameter Struktur enthält Parameter für den [**MCI- \_ Wiedergabe**](mci-play.md) Befehl für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
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

**dwat**
</dt> <dd>

Der Uhrzeitwert, der sich auf den Befehl [**MCI \_ Play**](mci-play.md) oder [**\_ MCI**](mci-cue.md) -Hinweis auswirkt. Bei der Wiedergabe von [**MCI \_ ist**](mci-play-parms.md)dies der Zeitpunkt, zu dem die Wiedergabe beginnt. Bei **MCI \_**-Hinweis ist dies die Zeit, zu der das cubegerät die in **dwfrom** angegebene Position erreicht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Positionen werden im aktuellen Zeitformat angegeben.

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ -Hinweis**](mci-cue.md)
</dt> <dt>

[**MCI- \_ Play**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

