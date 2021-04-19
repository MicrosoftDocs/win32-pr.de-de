---
description: Die tapicontrolflags-Enumeration wird von einer Reihe von Methoden verwendet, um anzugeben, ob eine bestimmte Eigenschaft automatisch oder manuell gesteuert wird.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Tapicontrolflags-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356038"
---
# <a name="tapicontrolflags-enumeration"></a>Tapicontrolflags-Enumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **tapicontrolflags** -Enumeration wird von einer Reihe von Methoden verwendet, um anzugeben, ob eine bestimmte Eigenschaft automatisch oder manuell gesteuert wird.

## <a name="syntax"></a>Syntax


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**Tapicontrol- \_ Flags " \_ None"**
</dt> <dd>

TAPI weist keine steuerungflags für die Eigenschaft auf.

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**Tapicontrol- \_ Flags \_ automatisch**
</dt> <dd>

Die-Eigenschaft wird automatisch gesteuert.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**Tapicontrol- \_ Flags \_ manuell**
</dt> <dd>

Die-Eigenschaft wird manuell gesteuert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itaudiodebug econtrol:: GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**Itaudiodebug econtrol:: Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**Itaudiode vicecontrol:: Set**](itaudiodevicecontrol-set.md)
</dt> <dt>

[**Itaudiosettings:: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**Itaudiosettings:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**Itaudiosettings:: Set**](itaudiosettings-set.md)
</dt> <dt>

[**Itcallqualitycontrol:: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**Itcallqualitycontrol:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**Itcallqualitycontrol:: Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**Itstreamqualitycontrol:: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**Itstreamqualitycontrol:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**Itstreamqualitycontrol:: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




