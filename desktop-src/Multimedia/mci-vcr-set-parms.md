---
title: MCI_VCR_SET_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Set- \_ Parameter enthält Parameter für den MCI- \_ Befehl Set für Video-Kassetten-Recorder.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392152"
---
# <a name="mci_vcr_set_parms-structure"></a>Struktur der MCI- \_ VCR- \_ Set- \_ Parametern

Die Struktur der **MCI- \_ VCR- \_ Set \_** -Parameter enthält Parameter für den [**MCI-Befehl \_ Set**](mci-set.md) für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwtimeformat**
</dt> <dd>

Aktuelles Uhrzeit Format.

</dd> <dt>

**dwaudiodatei**
</dt> <dd>

Nicht verwendet.

</dd> <dt>

**dwtimemode**
</dt> <dd>

-Konstante, die die vom Gerät verwendete Zeit Steuerungs Quelle angibt. Bei der Zeit Steuerungs Quelle handelt es sich entweder um eine auf Videoband aufgezeichnete Zeit Leitzahl oder um die Leistungsindikatoren auf dem Gerät, die die videobandbewegung verstehen.

</dd> <dt>

**dwrecordformat**
</dt> <dd>

Aufzeichnungsrate.

</dd> <dt>

**dwcounter Format**
</dt> <dd>

Format eines neuen Leistungswert Werts.

</dd> <dt>

**dwIndex**
</dt> <dd>

Inhalt der Bildschirm Anzeige.

</dd> <dt>

**dwtracking**
</dt> <dd>

Beim Nachverfolgen der VCR-Wiedergabe Rate verwendete Geschwindigkeitsanpassung.

</dd> <dt>

**dwspeed**
</dt> <dd>

Wiedergabegeschwindigkeit, die vom Gerät als ganze Zahl verwendet wird. Die normale Wiedergabegeschwindigkeit ist 1000, doppelte Geschwindigkeit 2000 und halb Geschwindigkeit 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Die Länge des Videobands, wenn die Länge vom Gerät nicht erkennbar ist.

</dd> <dt>

**dwcounter**
</dt> <dd>

Neuer Leistungswert.

</dd> <dt>

**dwclock**
</dt> <dd>

Neue Uhrzeit.

</dd> <dt>

**dwpaustitimeout**
</dt> <dd>

Neuer Timeout Wert für den anhaltebefehl.

</dd> <dt>

**dwprerollduration**
</dt> <dd>

Die für die Stabilisierung der VCR-Ausgabe benötigte videobandlänge.

</dd> <dt>

**dwpostrollduration**
</dt> <dd>

Die für den VCR-Transport erforderliche Video Bandlänge, wenn ein [**MCI \_**](mci-stop.md) -Befehl zum Beenden oder ein [**MCI \_**](mci-pause.md) -anhaltebefehl ausgegeben wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

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

[**MCI- \_ Pause**](mci-pause.md)
</dt> <dt>

[**MCI- \_ Gruppe**](mci-set.md)
</dt> <dt>

[**MCI- \_ Beendigung**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

