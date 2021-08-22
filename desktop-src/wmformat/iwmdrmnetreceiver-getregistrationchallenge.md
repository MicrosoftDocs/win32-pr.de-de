---
title: IWMDRMNetReceiver GetRegistrationChallenge-Methode (Wmdrmsdk.h)
description: Die GetRegistrationChallenge-Methode generiert eine meldung Windows Media DRM for Network Devices registration challenge (Medien-DRM für Netzwerkgeräte– Registrierungs-Challenge).
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- 'GetRegistrationChallenge-Methode : Windows Media Format'
- GetRegistrationChallenge-Methode windows Media Format, IWMDRMNetReceiver-Schnittstelle
- IWMDRMNetReceiver-Schnittstelle Windows Media Format , GetRegistrationC wiege-Methode
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
ms.openlocfilehash: 7f6c066de9c455006bfa7e500a30ac290299956ba03a6b4d8df6652a60a75a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701035"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>IWMDRMNetReceiver::GetRegistrationChallenge-Methode

Die **GetRegistrationChallenge-Methode** generiert eine meldung Windows Media DRM for Network Devices registration challenge (Medien-DRM für netzwerkgeräteregistrierung).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbRegistrationCppege* \[ out\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der generierten Herausforderung empfängt. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher durch Aufrufen von **CoTaskMemFree frei geben.**

</dd> <dt>

*–RegistrationC wiege* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Registrierungsforderung in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMNetReceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





