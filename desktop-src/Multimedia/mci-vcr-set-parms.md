---
title: MCI_VCR_SET_PARMS-Struktur (Vcr.h)
description: Die MCI \_ VCR \_ SET \_ PARMS-Struktur enthält Parameter für den MCI \_ SET-Befehl für Video-Cassette-Aufzeichnungen.
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
ms.openlocfilehash: 9fe32f93500ae4c294bad372868e9f7818c672824611bcbc29c3315eb75a9742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802985"
---
# <a name="mci_vcr_set_parms-structure"></a>MCI \_ VCR \_ SET \_ PARMS-Struktur

Die **MCI \_ VCR \_ SET \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ SET-Befehl**](mci-set.md) für Video-Cassette-Aufzeichnungen.

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

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Aktuelles Zeitformat.

</dd> <dt>

**dwAudio**
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

**dwTimeMode**
</dt> <dd>

Konstante, die die vom Gerät verwendete Zeitsteuerungsquelle angibt. Die Zeitsteuerungsquelle ist entweder ein Zeitcode, der auf videotape aufgezeichnet wurde, oder die Indikatoren auf dem Gerät, die videotape movement (Videobandbewegung) verstehen.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Aufzeichnungsrate.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Format eines neuen Indikatorzeitwerts.

</dd> <dt>

**dwIndex**
</dt> <dd>

Inhalt der Anzeige auf dem Bildschirm.

</dd> <dt>

**dwTracking**
</dt> <dd>

Geschwindigkeitsanpassung, die beim Nachverfolgen der VCR-Wiedergaberate verwendet wird.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Wiedergabegeschwindigkeit, die vom Gerät als ganze Zahl verwendet wird. Die normale Wiedergabegeschwindigkeit beträgt 1000, die doppelte Geschwindigkeit 2000 und die halbe Geschwindigkeit 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Videobandlänge, wenn die Länge vom Gerät nicht erkannt werden kann.

</dd> <dt>

**dwCounter**
</dt> <dd>

Neuer Indikatorwert.

</dd> <dt>

**dwClock**
</dt> <dd>

Neue Uhrzeit.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Neuer Timeoutwert für den Befehl "pause".

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Videotapelänge, die erforderlich ist, um die VCR-Ausgabe zu stabilieren.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

Videotapelänge, die erforderlich ist, um den VCR-Transport abzuleiten, wenn ein [**MCI \_ STOP-**](mci-stop.md) oder [**MCI \_ PAUSE-Befehl**](mci-pause.md) ausgegeben wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ PAUSE**](mci-pause.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**MCI \_ STOP**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

