---
title: MCI_WAVE_SET_PARMS -Struktur (Mciapi.h)
description: Die MCI \_ WAVE \_ SET \_ PARMS-Struktur enthält Informationen zum MCI \_ SET-Befehl für Waveform-Audiogeräte.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85508ec493ecdc38825b90877e608683fe6c0bb7c099365c187a434890c605d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783750"
---
# <a name="mci_wave_set_parms-structure"></a>MCI \_ WAVE \_ SET \_ PARMS-Struktur

Die **MCI \_ WAVE SET \_ \_ PARMS-Struktur** enthält Informationen zum [**MCI \_ SET-Befehl**](mci-set.md) für Waveform-Audiogeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Das Zeitformat des Geräts.

</dd> <dt>

**dwAudio**
</dt> <dd>

Kanalnummer für Audioausgabe. Wird normalerweise verwendet, wenn ein Kanal ein- oder ausgeschaltet wird.

</dd> <dt>

**wInput**
</dt> <dd>

Audioeingabekanal.

</dd> <dt>

**wOutput**
</dt> <dd>

Das zu verwendende Ausgabegerät. Dieser Wert kann beispielsweise 2 sein, wenn auf einem System zwei Soundkarten installiert sind.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Format der Waveform-Audiodaten, z. B. WAVE \_ FORMAT \_ PCM. Mögliche Werte werden in Mmreg.h definiert.

</dd> <dt>

**wReserved2**
</dt> <dd>

Reserviert.

</dd> <dt>

**nChannels**
</dt> <dd>

Mono (1) oder Stereo (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Reserviert.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Beispiele pro Sekunde.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Abtastrate in Bytes pro Sekunde.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Blockiert die Ausrichtung der Daten.

</dd> <dt>

**wReserved4**
</dt> <dd>

Reserviert.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits pro Beispiel.

</dd> <dt>

**wReserved5**
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

