---
title: MCI_WAVE_SET_PARMS-Struktur (mciapi. h)
description: Die Struktur von MCI \_ \_ -Wellen Satz \_ -Parametern enthält Informationen zum MCI \_ -Befehl Set für Waveform-Audiogeräte.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS Struktur Windows Multimedia
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
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859221"
---
# <a name="mci_wave_set_parms-structure"></a>Struktur von MCI- \_ Wellen \_ Satz- \_ Parametern

Die Struktur von **MCI- \_ Wellen \_ Satz- \_ Parametern** enthält Informationen zum [**MCI-Befehl \_ Set**](mci-set.md) für Waveform-Audiogeräte.

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

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwtimeformat**
</dt> <dd>

Das Zeitformat des Geräts.

</dd> <dt>

**dwaudiodatei**
</dt> <dd>

Die Kanalnummer für die Audioausgabe. Wird normalerweise verwendet, wenn ein Kanal ein-oder ausgeschaltet wird.

</dd> <dt>

**Winput**
</dt> <dd>

Audioeingabechannel.

</dd> <dt>

**woutput**
</dt> <dd>

Ausgabegerät, das verwendet werden soll. Dieser Wert kann z. b. 2 lauten, wenn ein System über zwei installierte Soundkarten verfügt.

</dd> <dt>

**wformattag**
</dt> <dd>

Format der Waveform-Audiodaten, z. b. Wave- \_ Format \_ PCM. Mögliche Werte sind in "mmreg. h" definiert.

</dd> <dt>

**wReserved2**
</dt> <dd>

Reserviert.

</dd> <dt>

**nchannels**
</dt> <dd>

Mono (1) oder Stereo (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Reserviert.

</dd> <dt>

**nsamplespersec**
</dt> <dd>

Stichproben pro Sekunde.

</dd> <dt>

**navgbytespersec**
</dt> <dd>

Die Stichprobenrate in Byte pro Sekunde.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Blockieren der Ausrichtung der Daten.

</dd> <dt>

**wReserved4**
</dt> <dd>

Reserviert.

</dd> <dt>

**wbitspersample**
</dt> <dd>

Bits pro Stichprobe.

</dd> <dt>

**wReserved5**
</dt> <dd>

Reserviert.

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

[**MCI- \_ Gruppe**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

