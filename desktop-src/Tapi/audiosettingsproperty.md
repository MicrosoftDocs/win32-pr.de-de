---
description: 'Die audiosettingsproperty-Enumeration wird von den Methoden itaudiosettings:: GetRange, itaudiosettings:: Get und itaudiosettings:: Set verwendet, um anzugeben, welche audioeinstellungs Eigenschaft adressiert wird.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Audiosettingsproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368448"
---
# <a name="audiosettingsproperty-enumeration"></a>Audiosettingsproperty-Enumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **audiosettingsproperty** -Enumeration wird von den Methoden [**itaudiosettings:: GetRange**](itaudiosettings-getrange.md), [**itaudiosettings:: Get**](itaudiosettings-get.md)und [**itaudiosettings:: Set**](itaudiosettings-set.md) verwendet, um anzugeben, welche audioeinstellungs Eigenschaft adressiert wird.

## <a name="syntax"></a>Syntax


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**Audiosettings \_ Signallevel**
</dt> <dd>

Signsettings-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**Audiosettings- \_ silencethreshold**
</dt> <dd>

Eigenschaft für den Ruhe Schwellenwert.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**Audiosettings- \_ Volume**
</dt> <dd>

Volume-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**Audiosettings- \_ Saldo**
</dt> <dd>

Balance-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**Audiosettings- \_ Lautstärke**
</dt> <dd>

Lautstärke-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**Audiosettings- \_ Treble**
</dt> <dd>

Treble-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**Audiosettings- \_ Bass**
</dt> <dd>

Bass-Eigenschaft.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**Audiosettings \_ Mono**
</dt> <dd>

Die monaural-Eigenschaft.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itaudiosettings:: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**Itaudiosettings:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**Itaudiosettings:: Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




