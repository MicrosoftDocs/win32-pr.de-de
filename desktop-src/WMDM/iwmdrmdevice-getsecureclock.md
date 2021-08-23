---
title: IWMDRMDevice GetSecureClock-Methode
description: Die GetSecureClock-Methode ruft die sichere Uhr ab, sodass zeitbasierte Lizenzen erzwungen werden können.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- GetSecureClock-Methode windows Media Geräte-Manager
- GetSecureClock-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice interface windows Media Geräte-Manager , GetSecureClock method
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa9494a594a396550028f083cc2b646f2093f6369ab27ae5494bf70c13628d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619780"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>IWMDRMDevice::GetSecureClock-Methode

Die **GetSecureClock-Methode** ruft die sichere Uhr ab, sodass zeitbasierte Lizenzen erzwungen werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppbSecureClock* \[ out\]
</dt> <dd>

Abgerufene sichere Uhr.

</dd> <dt>

*–secureClock* \[ out\]
</dt> <dd>

Größe der sicheren Uhr in Bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Gerätestatusflags. Dieser Wert muss eines der folgenden Flags sein.



| Flag                     | Beschreibung                            |
|--------------------------|----------------------------------------|
| \_WMDRM-GERÄT \_ ISWMDRM   | Das Gerät unterstützt Windows Medien-DRM. |
| WMDRM \_ DEVICE \_ NEEDCLOCK | Das Gerät benötigt uhr.                |
| \_WMDRM-GERÄT \_ WIDERRUFEN   | Das Gerät wurde widerrufen.           |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetSecureClockCuhrge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





