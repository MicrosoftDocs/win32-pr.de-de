---
description: Die GetCurrentFormat-Methode ruft das Medienformat des aktuellen Streams ab.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: ITFormatControl::GetCurrentFormat-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d261cd88a9aac4998f15d871a20408aecb367b793b78b7f9fcaeff452273a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140333"
---
# <a name="itformatcontrolgetcurrentformat-method"></a>ITFormatControl::GetCurrentFormat-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetCurrentFormat-Methode** ruft das Medienformat des aktuellen Streams ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMediaType* \[ out\]
</dt> <dd>

Zeiger auf einen **AM \_ MEDIA TYPE-Deskriptor \_** des Terminalformats. Weitere Informationen zu **AM \_ MEDIA \_ TYPE** finden Sie in der DirectX-Dokumentation.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |



 

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
</dt> </dl>

 

 




