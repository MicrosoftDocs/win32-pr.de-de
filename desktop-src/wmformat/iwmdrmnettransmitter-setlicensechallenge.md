---
title: IWMDRMNetTransmitter SetLicenseChallenge-Methode (Wmdrmsdk.h)
description: Die SetLicenseChallenge-Methode verarbeitet eine Lizenzaufforderung, die von einem Windows Medien-DRM für den Empfänger von Netzwerkgeräten gesendet wird.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- SetLicenseChallenge-Methode windows Media Format
- SetLicenseChallenge-Methode windows Media Format , IWMDRMNetTransmitter-Schnittstelle
- IWMDRMNetTransmitter-Schnittstelle windows Media Format , SetLicenseChallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027568"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>IWMDRMNetTransmitter::SetLicenseChallenge-Methode

Die **SetLicenseChallenge-Methode** verarbeitet eine Lizenzaufforderung, die von einem Windows Medien-DRM für den Empfänger von Netzwerkgeräten gesendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbLicenseChallenge* \[ In\]
</dt> <dd>

Zeiger auf die Lizenzaufforderungsdaten, die von einem Empfänger gesendet wurden.

</dd> <dt>

*cbLicenseChallenge* \[ In\]
</dt> <dd>

Größe der Lizenzaufforderung in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn diese Methode erfolgreich ist, verwenden nachfolgende Aufrufe der anderen Methoden von **IWMDRMNetTransmitter** die Informationen in der verarbeiteten Abfrage.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMNetTransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





