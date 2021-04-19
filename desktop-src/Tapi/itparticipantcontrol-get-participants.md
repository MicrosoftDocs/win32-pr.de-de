---
description: Die \_ Methode Get participants erstellt eine Sammlung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Itparticipantcontrol:: get_Participants-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370055"
---
# <a name="itparticipantcontrolget_participants-method"></a>Itparticipantcontrol:: get- \_ Teilnehmer Methode

\[**get \_ Teilnehmer** sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Methode **get \_ participants** erstellt eine Sammlung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind. Diese Methode wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. in Visual Basic. C-und C++-Anwendungen müssen die [**enumerateparticipants**](itparticipantcontrol-enumerateparticipants.md) -Methode verwenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvariant* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine **Variante** , die eine [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) von [**itteilnehmer**](itparticipant.md) -Schnittstellen Zeigern enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *pvariant* -Parameter ist kein gültiger Zeiger.<br/>     |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode für die [**itparticipants**](itparticipant.md) -Schnittstelle auf, die von **itparticipantcontrol:: get- \_ Teilnehmern** zurückgegeben Die Anwendung muss Release auf der **itparticipants** -Schnittstelle aufzurufen, um Ihnen zugeordnete Ressourcen frei **zugeben** .

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

[**Enumerateparticipants**](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[**Itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> </dl>

 

 




