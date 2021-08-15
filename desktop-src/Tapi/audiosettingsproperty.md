---
description: Die AudioSettingsProperty-Enum wird von den Methoden ITAudioSettings::GetRange, ITAudioSettings::Get und ITAudioSettings::Set verwendet, um die adressierte Audioeinstellungseigenschaft anzugeben.
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: AudioSettingsProperty-Enumeration (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b15cfb5a0211f02ac333ba75e47b5e4cbd5c44865b4a18c2f19ea3a8769dde3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871530"
---
# <a name="audiosettingsproperty-enumeration"></a>AudioSettingsProperty-Enumeration

\[Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **AudioSettingsProperty-Enum** wird von den [**Methoden ITAudioSettings::GetRange,**](itaudiosettings-getrange.md) [**ITAudioSettings::Get**](itaudiosettings-get.md)und [**ITAudioSettings::Set**](itaudiosettings-set.md) verwendet, um die adressierte Audioeinstellungseigenschaft anzugeben.

## <a name="syntax"></a>Syntax


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Signaleinstellungseigenschaft.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Eigenschaft für Ruheschwellenwert.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings-Volume \_**
</dt> <dd>

Volumeeigenschaft.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ Balance**
</dt> <dd>

Balance-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_AudioSettings-Lautheit**
</dt> <dd>

Lautheitseigenschaft.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ Treble**
</dt> <dd>

Treble-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**\_AudioSettings(AudioSettings)**
</dt> <dd>

Eigenschaft "Eigenschaften".

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ Mono**
</dt> <dd>

Aturural-Eigenschaft.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings::Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings::Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




