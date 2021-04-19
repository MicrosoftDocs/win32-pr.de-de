---
description: Die get \_ Streams-Methode erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Itteilnehmer:: get_Streams-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368527"
---
# <a name="itparticipantget_streams-method"></a>Itteilnehmer:: get \_ Streams-Methode

\[**get \_ Streams** sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **get \_ Streams** -Methode erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind. Diese Methode wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. in Visual Basic. C-und C++-Anwendungen müssen die [**enumeratestreams**](itparticipant-enumeratestreams.md) -Methode verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvariant* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine **Variante** , die eine [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) von [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstellen Zeigern enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pvariant* -Parameter ist kein gültiger Zeiger.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode für die [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle auf, die von **itparticipants:: get \_ Streams** zurückgegeben wurde. Die Anwendung muss Release auf der **itstream** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

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

[**Enumeratestreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**Ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**Itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**Itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

