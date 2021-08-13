---
description: Die GetStreamCaps-Methode ruft die Funktionen ab, die einem angegebenen Formatindex zugeordnet sind.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: ITFormatControl::GetStreamCaps-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f54cbd44a946c0fcd3cf297c4cacadc49369765b8c1b6505031a145768c3b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406110"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>ITFormatControl::GetStreamCaps-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetStreamCaps-Methode** ruft die Funktionen ab, die einem angegebenen Formatindex zugeordnet sind.

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

*dwIndex* \[ In\]
</dt> <dd>

Index des formats, das untersucht wird.

</dd> <dt>

*ppMediaType* \[ out\]
</dt> <dd>

Zeiger auf einen **AM \_ MEDIA TYPE-Deskriptor \_** des Terminalformats. Weitere Informationen zu **AM \_ MEDIA TYPE \_ finden** Sie in der DirectX-Dokumentation.

</dd> <dt>

*pStreamConfigCaps* \[ out\]
</dt> <dd>

Eine [**TAPI \_ STREAM \_ CONFIG \_ CAPS-Struktur,**](tapi-stream-config-caps.md) die ausführliche Informationen zu Den Streamfunktionen bietet.

</dd> <dt>

*pfEnabled* \[ out\]
</dt> <dd>

Gibt an, ob das dem aktuellen Index zugeordnete Format aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




