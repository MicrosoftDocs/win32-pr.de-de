---
description: Mit der enumeratestreams-Methode werden Datenströme aufgelistet, die derzeit mit den Teilnehmern erstellt werden. Diese Methode wird für C-und C++-Anwendungen bereitgestellt. Automatisierungs Client Anwendungen, wie z. b. die in Visual Basic geschriebenen, müssen die get \_ Streams-Methode verwenden.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Itparticipants:: enumeratestreams-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358646"
---
# <a name="itparticipantenumeratestreams-method"></a>Itparticipants:: enumeratestreams-Methode

\[**Enumeratestreams** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **enumeratestreams** -Methode werden Datenströme aufgelistet, die derzeit mit den Teilnehmern erstellt werden. Diese Methode wird für C-und C++-Anwendungen bereitgestellt. Automatisierungs Client Anwendungen, wie z. b. die in Visual Basic geschriebenen, müssen die [**get \_ Streams**](itparticipant-get-streams.md) -Methode verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *pprestream* \[ " vorgenommen\]
</dt> <dd>

Zeiger auf den [**ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) -Schnittstellen Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Der Parameter " *dereumstream* " ist kein gültiger Zeiger.<br/> |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode für die [**ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) -Schnittstelle auf, die von **itparticipants:: enumeratestreams** zurückgegeben wird. Die Anwendung muss Release auf der **ienumstream** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> <dt>

[**Daten \_ Ströme erhalten**](itparticipant-get-streams.md)
</dt> <dt>

[**Ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




