---
description: Die Von den Methoden ITStreamQualityControl::GetRange, ITStreamQualityControl::Get und ITStreamQualityControl::Set verwendete StreamQualityProperty-Enum, um die adressierte Streamqualitätseigenschaft anzugeben.
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: StreamQualityProperty-Enumeration (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea006b614522ffcab6f96e630df03087b78864ff7d7af6ddcd5c515bc090e821
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905750"
---
# <a name="streamqualityproperty-enumeration"></a>StreamQualityProperty-Enumeration

\[Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die Von den Methoden [**ITStreamQualityControl::GetRange,**](itstreamqualitycontrol-getrange.md) [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md)und [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) verwendete **StreamQualityProperty-Enum,** um die adressierte Streamqualitätseigenschaft anzugeben.

## <a name="syntax"></a>Syntax


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**
</dt> <dd>

Maximale Bitrate.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**
</dt> <dd>

Minimale Bitrate.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**
</dt> <dd>

Maximales Frameintervall.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**
</dt> <dd>

Minimales Frameintervall.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




