---
description: Die \_ Methode Get mediatypes Ruft die einem Teilnehmer zugeordneten Medientypen ab.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Itteilnehmer:: get_MediaTypes-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358206"
---
# <a name="itparticipantget_mediatypes-method"></a>Itteilnehmer:: get \_ mediatypes-Methode

\[**get \_ Mediatypes** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Methode **get \_ mediatypes** Ruft die einem Teilnehmer zugeordneten [**Medientypen**](tapimediatype--constants.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plmediatype* \[ vorgenommen\]
</dt> <dd>

Zeiger auf Medientyp-Flags, z. b. tapimediatype \_ Video.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *plmediatype* -Parameter ist kein gültiger Zeiger.<br/>  |



 

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

[**Medientypen**](tapimediatype--constants.md)
</dt> </dl>

 

 




