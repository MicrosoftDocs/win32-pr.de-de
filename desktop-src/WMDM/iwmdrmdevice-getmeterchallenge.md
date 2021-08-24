---
title: IWMDRMDevice GetMeterChallenge-Methode
description: Die GetMeterChallenge-Methode ruft die Messungsforderung ab.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- GetMeterChallenge-Methode windows Media Geräte-Manager
- GetMeterChallenge-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice-Schnittstelle windows Media Geräte-Manager , GetMeterChallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ccccf8ffe17bdcbf25c89830e34e7a52294a6c661bc4b7d9193afd215246cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766630"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>IWMDRMDevice::GetMeterChallenge-Methode

Die **GetMeterChallenge-Methode** ruft die Messungsforderung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrMeterCert* \[ In\]
</dt> <dd>

Messungszertifikat, das der Inhaltsbesitzer zum Sammeln der zugeordneten Messungsdaten auf dem Gerät an den Hostcomputer sendet

</dd> <dt>

*ppbMeterC wiege* \[ out\]
</dt> <dd>

Abgerufenes Messungs-Challenge-Ergebnis.

</dd> <dt>

*-MeterC wiege* \[ out\]
</dt> <dd>

Die Größe der Messungsforderung in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Messdaten werden gesammelt und im DRM-Datenspeicher auf dem Gerät für Inhalte mit aktivierter Messung gespeichert. Aktionen wie wiedergabe werden aufgezeichnet. Wenn diese Funktion aufgerufen wird, sammelt das Gerät die Messdaten im DRM-Datenspeicher in Form eines XML-Dokuments und sendet sie an den Hostcomputer. Wenn zu viele Daten gespeichert sind, werden sie in Phasen gesendet.

Wenn der Hostcomputer die Messungsdaten empfängt, sendet er die Daten über das Internet an die im Messungszertifikat angegebene URL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





