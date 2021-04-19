---
description: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Ienumtime:: Clone-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369238"
---
# <a name="ienumtimeclone-method"></a>Ienumtime:: Clone-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Clone** -Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das neue [**ienumtime**](ienumtime.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppum* -Parameter ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>  | Aus unbekannten Gründen fehlgeschlagen.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode für die [**ienumtime**](ienumtime.md) -Schnittstelle auf, die von **ienumtime:: Clone** zurückgegeben wurde. Die Anwendung muss Release auf der **ienumtime** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumtime**](ienumtime.md)
</dt> </dl>

 

 




