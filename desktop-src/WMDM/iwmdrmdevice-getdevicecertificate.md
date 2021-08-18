---
title: IWMDRMDevice GetDeviceCertificate-Methode
description: Die GetDeviceCertificate-Methode ruft das Gerätezertifikat ab.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- GetDeviceCertificate-Methode windows Media Geräte-Manager
- GetDeviceCertificate-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice-Schnittstelle windows Media Geräte-Manager , GetDeviceCertificate-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299233ff4344f44535933221141534ab2b0173ba54e47c9cc340020a2f462eb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619820"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a>IWMDRMDevice::GetDeviceCertificate-Methode

Die **GetDeviceCertificate-Methode** ruft das Gerätezertifikat ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrDevCert* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der das abgerufene Gerätezertifikat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





