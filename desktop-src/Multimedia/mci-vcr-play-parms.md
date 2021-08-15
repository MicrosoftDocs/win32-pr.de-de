---
title: MCI_VCR_PLAY_PARMS -Struktur (Vcr.h)
description: Die MCI \_ VCR \_ PLAY \_ PARMS-Struktur enthält Parameter für den MCI \_ PLAY-Befehl für Video cassette-Aufzeichnungen.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS-Struktur Windows Multimedia
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
ms.openlocfilehash: 6f2e725ca3dc04fa13dd89aff0a5fbd60ede66f83154740803c98679eb77aec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374359"
---
# <a name="mci_vcr_play_parms-structure"></a>MCI \_ VCR \_ PLAY \_ PARMS-Struktur

Die **MCI \_ VCR \_ PLAY \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ PLAY-Befehl**](mci-play.md) für Video cassette-Aufzeichnungen.

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

**dwAt**
</dt> <dd>

Zeitwert, der den [**MCI \_ PLAY- oder**](mci-play.md) [**MCI \_ CUE-Befehl**](mci-cue.md) beeinflusst. Bei [**MCI \_ PLAY**](mci-play-parms.md)ist dies der Zeitpunkt, zu dem die Wiedergabe beginnt. Für **MCI \_ CUE** ist dies der Zeitpunkt, zu dem das Cued-Gerät die in **dwFrom gegebene Position erreicht.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Positionen werden im aktuellen Zeitformat angegeben.

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**MCI \_ PLAY**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

