---
description: Die getcurrentformat-Methode ruft das Medienformat des aktuellen Streams ab.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Itformatcontrol:: getcurrentformat-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355941"
---
# <a name="itformatcontrolgetcurrentformat-method"></a>Itformatcontrol:: getcurrentformat-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **getcurrentformat** -Methode ruft das Medienformat des aktuellen Streams ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PpMediaType* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **am \_ \_ Medientyp** Deskriptor des Terminal Formats. Weitere Informationen zu dem **\_ \_ Medientyp** finden Sie in der DirectX-Dokumentation.

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

[**Itformatcontrol**](itformatcontrol.md)
</dt> </dl>

 

 




