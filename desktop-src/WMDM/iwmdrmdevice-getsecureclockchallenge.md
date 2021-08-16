---
title: IWMDRMDevice GetSecureClockChallenge-Methode
description: Die GetSecureClockChallenge-Methode ruft das Ergebnis der Herausforderung der sicheren Uhr ab.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- GetSecureClockCuhrge-Methode windows Media Geräte-Manager
- GetSecureClockChallenge-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice interface windows Media Geräte-Manager , GetSecureClockChallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957250"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>IWMDRMDevice::GetSecureClockChallenge-Methode

Die **GetSecureClockChallenge-Methode** ruft das Ergebnis der Herausforderung der sicheren Uhr ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbC wiege* \[ out\]
</dt> <dd>

Abgerufenes Ergebnis der Herausforderung.

</dd> <dt>

*beiC wiege* \[ out\]
</dt> <dd>

Größe des Challenge-Ergebnisses in Bytes.

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

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





