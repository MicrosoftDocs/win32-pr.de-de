---
title: Iwmdrmnetreceiver processlicenseresponse-Methode (wmdrmsdk. h)
description: Die processlicenseresponse-Methode verarbeitet die vom Sender gesendete Lizenz Antwort als Antwort auf eine Lizenz Herausforderung.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Processlicenseresponse-Methode Windows Media-Format
- Processlicenseresponse-Methode, Windows Media-Format, iwmdrmnetreceiver-Schnittstelle
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, processlicenseresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357563"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>Iwmdrmnetreceiver::P rocess licenseresponse-Methode

Die **processlicenseresponse** -Methode verarbeitet die vom Sender gesendete Lizenz Antwort als Antwort auf eine Lizenz Herausforderung.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pblicenseresponse* \[ in\]
</dt> <dd>

Vom Sender empfangene Lizenz Antwort.

</dd> <dt>

*cblicenseresponse* \[ in\]
</dt> <dd>

Größe der Antwort in Bytes.

</dd> <dt>

*ppbwmdrmnetlicenserepresentation* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Adresse der internen Lizenz Darstellung für die in der Lizenz Antwortnachricht enthaltene Lizenz empfängt. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen. Dieser Parameter kann auf **null** festgelegt werden, wenn die Lizenz Darstellung nicht benötigt wird.

</dd> <dt>

*pcbwmdrmnetlicenserepresentation* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Lizenz Darstellung erhält. Muss auf **null** festgelegt werden, wenn *ppbwmdrmnetlicenserepresentation* **null** ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt> </dl> | Es wird eine aktualisierte Inhalts Sperr Liste benötigt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Die mit dieser Methode verarbeitete Lizenz Antwort muss der letzten Lizenz Herausforderung entsprechen, die auf dem Client Computer generiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnetreceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Iwmdrmnetreceiver:: getlicensechallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





