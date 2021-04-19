---
title: Iwmdrmnetreceiver getlicensechallenge-Methode (wmdrmsdk. h)
description: Mit der getlicencchallenge-Methode wird eine Windows Media DRM for Network Devices-Lizenz Aufforderung generiert, die beim Anfordern geschützter Inhalte an einen Sender gesendet werden kann.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Getlicencchallenge-Methode, Windows Media-Format
- Getlicensechallenge-Methode, Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, getlicensechallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370590"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>Iwmdrmnetreceiver:: getlicensechallenge-Methode

Mit der **getlicencchallenge** -Methode wird eine Windows Media DRM for Network Devices-Lizenz Aufforderung generiert, die beim Anfordern geschützter Inhalte an einen Sender gesendet werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAction* \[ in\]
</dt> <dd>

Die Aktion, für die die Herausforderung generiert werden soll.

</dd> <dt>

*ppblicenabchallenge* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers, der auf die Adresse der generierten Challenge festgelegt ist. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.

</dd> <dt>

*pcblicenanchallenge* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Lizenz Herausforderung in Bytes erhält.

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

[**Iwmdrmnetreceiver::P rocess licenseresponse**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





