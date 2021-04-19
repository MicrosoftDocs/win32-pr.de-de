---
description: Die getstreamcaps-Methode ruft die Funktionen ab, die einem bestimmten Format Index zugeordnet sind.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Itformatcontrol:: getstreamcaps-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367660"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>Itformatcontrol:: getstreamcaps-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **getstreamcaps** -Methode ruft die Funktionen ab, die einem bestimmten Format Index zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Der Index des zu überprüfenden Formats.

</dd> <dt>

*PpMediaType* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **am \_ \_ Medientyp** Deskriptor des Terminal Formats. Weitere Informationen zu dem **\_ \_ Medientyp** finden Sie in der DirectX-Dokumentation.

</dd> <dt>

*pstreamconfigcaps* \[ vorgenommen\]
</dt> <dd>

Eine [**TAPI-Daten \_ Strom- \_ config \_**](tapi-stream-config-caps.md) -Struktur, die ausführliche Informationen zu Stream-Funktionen enthält.

</dd> <dt>

*pfaktivierte* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob das mit dem aktuellen Index verknüpfte Format aktiviert ist.

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
</dt> <dt>

[**TAPI \_ - \_ streamkonfigurationscaps \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




