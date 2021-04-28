---
description: 'IEnumTime::Clone-Methode: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: IEnumTime::Clone-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406dac1fad611ee5d3cb6c8b6ef32dfdb62cc963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090738"
---
# <a name="ienumtimeclone-method"></a>IEnumTime::Clone-Methode

\[ Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Clone-Methode** erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Zeiger auf das neue [**IEnumTime-Objekt.**](ienumtime.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppEnum-Parameter* ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Fehler aus unbekannten Gründen.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

TAPI ruft die **AddRef-Methode** für die [**IEnumTime-Schnittstelle**](ienumtime.md) auf, die von **IEnumTime::Clone** zurückgegeben wird. Die Anwendung muss **Release** auf der **IEnumTime-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




