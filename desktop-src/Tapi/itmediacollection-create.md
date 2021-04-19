---
description: Die Create-Methode erstellt ein neues Medium mit Standardeigenschaften, fügt es der Collection am angegebenen Index hinzu und gibt einen Zeiger auf die ITmedia-Schnittstelle zurück.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Itmediacollection:: Create-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370904"
---
# <a name="itmediacollectioncreate-method"></a>Itmediacollection:: Create-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Create** -Methode erstellt ein neues Medium mit Standardeigenschaften, fügt es der Collection am angegebenen Index hinzu und gibt einen Zeiger auf die [**ITmedia**](itmedia.md) -Schnittstelle zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index für das neue Element. Der minimale Wert für den Index ist 1, und der Höchstwert für den Index ist die aktuelle Anzahl von Elementen + 1.

</dd> <dt>

*ppmedia* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die erstellte [**ITmedia**](itmedia.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppmedia* -Parameter ist kein gültiger Zeiger.<br/>      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *Index* -Parameter ist ungültig.<br/>                  |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die meisten C-und C++-Listen sind 0-basiert, aber dieser Index basiert auf Visual Basic Kompatibilität, d. h., das erste Element hat eine Indexnummer von 1.

TAPI Ruft die **adressf** -Methode auf der [**ITmedia**](itmedia.md) -Schnittstelle auf, die von **itmediacollection:: Create** zurückgegeben wurde. Die Anwendung muss Release auf der [**ITmedia**](itmedia.md) -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITmedia**](itmedia.md)
</dt> <dt>

[**Itmediacollection**](itmediacollection.md)
</dt> </dl>

 

 




