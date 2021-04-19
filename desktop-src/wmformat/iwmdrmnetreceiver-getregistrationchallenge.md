---
title: Iwmdrmnetreceiver getregistrationchallenge-Methode (wmdrmsdk. h)
description: Mit der getregistrationchallenge-Methode wird eine Anforderungs Nachricht für die Registrierung von Windows Media DRM für Netzwerkgeräte generiert.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Getregistrationchallenge-Methode Windows Media-Format
- Getregistrationchallenge-Methode Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, getregistrationchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356034"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>Iwmdrmnetreceiver:: getregistrationchallenge-Methode

Mit der **getregistrationchallenge** -Methode wird eine Anforderungs Nachricht für die Registrierung von Windows Media DRM für Netzwerkgeräte generiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbregistrationchallenge* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der generierten Herausforderung empfängt. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.

</dd> <dt>

*pcbregistrationchallenge* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Registrierungs Herausforderung in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnetreceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Iwmdrmnetreceiver::P rocess RegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





