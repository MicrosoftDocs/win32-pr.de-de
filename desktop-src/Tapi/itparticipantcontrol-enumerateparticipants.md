---
description: Mit der enumerateparticipants-Methode werden die der aktuellen Konferenz zugeordneten Teilnehmer aufgelistet.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Itparticipantcontrol:: enumerateparticipants-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359218"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>Itparticipantcontrol:: enumerateparticipants-Methode

\[**Enumerateparticipants** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Mit der **enumerateparticipants** -Methode werden die der aktuellen Konferenz zugeordneten Teilnehmer aufgelistet. Diese Methode wird für C-und C++-Anwendungen bereitgestellt. Automatisierungs Client Anwendungen, wie z. b. die in Visual Basic geschriebenen, müssen die Methode [**get \_ participants**](itparticipantcontrol-get-participants.md) verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppumschlag-Teilnehmer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die [**ienumteilnehmer**](ienumparticipant.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                          |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der Parameter " *ppenumparticipants* " ist kein gültiger Zeiger.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode für die [**ienumteilnehmer**](ienumparticipant.md) -Schnittstelle auf, die von **itparticipantcontrol:: enumerateparticipants** zurückgegeben wurde. Die Anwendung muss Release auf der **ienumparticipants** -Schnittstelle aufzurufen, um Ihnen zugeordnete Ressourcen frei **zugeben** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itparticipantcontrol**](itparticipantcontrol.md)
</dt> <dt>

[**\_Teilnehmer erhalten**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**Ienumteilnehmer**](ienumparticipant.md)
</dt> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> </dl>

 

 




