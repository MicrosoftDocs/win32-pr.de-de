---
description: 'Die callqualityproperty-Enumeration wird von den Methoden itcallqualitycontrol:: GetRange, itcallqualitycontrol:: Get und itcallqualitycontrol:: Set verwendet, um anzugeben, dass die Eigenschaft Anruf Qualität adressiert wird.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Callqualityproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361540"
---
# <a name="callqualityproperty-enumeration"></a>Callqualityproperty-Enumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **callqualityproperty** -Enumeration wird von den Methoden [**itcallqualitycontrol:: GetRange**](itcallqualitycontrol-getrange.md), [**itcallqualitycontrol:: Get**](itcallqualitycontrol-get.md)und [**itcallqualitycontrol:: Set**](itcallqualitycontrol-set.md) verwendet, um anzugeben, dass die Eigenschaft Anruf Qualität adressiert wird.

## <a name="syntax"></a>Syntax


```C++
} CallQualityProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**Callquality- \_ controlinterval**
</dt> <dd>

Steuerungs Intervall.

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**Callquality- \_ confbitrate**
</dt> <dd>

Bitrate für die Konferenz.

</dd> <dt>

<span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**Callquality \_ maxinputbitrate**
</dt> <dd>

Maximale Eingabe Bitrate.

</dd> <dt>

<span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**Callquality \_ currinputbitrate**
</dt> <dd>

Aktuelle Eingabe Bitrate.

</dd> <dt>

<span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**Callquality \_ maxoutputbitrate**
</dt> <dd>

Maximale Ausgabe Bitrate.

</dd> <dt>

<span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**Callquality- \_ Cursor Cursor-Bitrate**
</dt> <dd>

Aktuelle Ausgabe Bitrate.

</dd> <dt>

<span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**Callquality \_ maxcpuload**
</dt> <dd>

Maximale CPU-Auslastung.

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**Callquality \_ currcpuload**
</dt> <dd>

Aktuelle CPU-Auslastung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itcallqualitycontrol:: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**Itcallqualitycontrol:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**Itcallqualitycontrol:: Set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




