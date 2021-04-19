---
description: 'Die streamqualityproperty-Enumeration, die von den itstreamqualitycontrol:: GetRange-, itstreamqualitycontrol:: Get-und itstreamqualitycontrol:: Set-Methoden verwendet wird, um anzugeben, welche Stream Quality-Eigenschaft adressiert wird.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Streamqualityproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362179"
---
# <a name="streamqualityproperty-enumeration"></a>Streamqualityproperty-Enumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **streamqualityproperty** -Enumeration, die von den [**itstreamqualitycontrol:: GetRange**](itstreamqualitycontrol-getrange.md)-, [**itstreamqualitycontrol:: Get**](itstreamqualitycontrol-get.md)-und [**itstreamqualitycontrol:: Set**](itstreamqualitycontrol-set.md) -Methoden verwendet wird, um anzugeben, welche Stream Quality-Eigenschaft adressiert wird.

## <a name="syntax"></a>Syntax


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**Streamquality- \_ maxbitrate**
</dt> <dd>

Maximale Bitrate.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**Streamquality- \_ currbitrate**
</dt> <dd>

Minimale Bitrate.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**Streamquality \_ minframeinterval**
</dt> <dd>

Maximales Frame Intervall.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**Streamquality \_ avgframeinterval**
</dt> <dd>

Minimaler Frame Intervall.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itstreamqualitycontrol:: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**Itstreamqualitycontrol:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**Itstreamqualitycontrol:: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




