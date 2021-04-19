---
description: Die GetRange-Methode ruft den Bereich gültiger Werte für eine angegebene audioeinstellungs Eigenschaft ab.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'Itaudiosettings:: GetRange-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369425"
---
# <a name="itaudiosettingsgetrange-method"></a>Itaudiosettings:: GetRange-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **GetRange** -Methode ruft den Bereich gültiger Werte für eine angegebene [**audioeinstellungs Eigenschaft**](audiosettingsproperty.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ in\]
</dt> <dd>

Member der [**audiosettingsproperty**](audiosettingsproperty.md) -Enumeration.

</dd> <dt>

*plmin* \[ vorgenommen\]
</dt> <dd>

Der minimale gültige Wert für die Input-Eigenschaft.

</dd> <dt>

*plmax* \[ vorgenommen\]
</dt> <dd>

Maximal gültiger Wert für die Eingabe Eigenschaft.

</dd> <dt>

*plsteppingdelta* \[ vorgenommen\]
</dt> <dd>

Inkrement, um den der Eigenschafts Wert vergrößert oder verkleinert werden kann.

</dd> <dt>

*pldefault* \[ vorgenommen\]
</dt> <dd>

Der Standardwert für den *Property* -Parameter.

</dd> <dt>

*plflags* \[ vorgenommen\]
</dt> <dd>

Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itaudiosettings**](itaudiosettings.md)
</dt> <dt>

[**Tapicontrolflags**](tapicontrolflags.md)
</dt> <dt>

[**Audiosettingsproperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




