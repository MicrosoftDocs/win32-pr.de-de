---
title: IWMDRMDevice SetLicenseResponse-Methode
description: Die SetLicenseResponse-Methode legt die Lizenzantwort fest.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- SetLicenseResponse-Methode windows Media Geräte-Manager
- SetLicenseResponse-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice interface windows Media Geräte-Manager , SetLicenseResponse method
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4161732002378449f196fdf83c4b880fcc2c02d345a0b08c6e6a464b81acb1dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055718"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>IWMDRMDevice::SetLicenseResponse-Methode

Die **SetLicenseResponse-Methode legt** die Lizenzantwort fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbResponse* \[ In\]
</dt> <dd>

Gibt die zu legende Antwort an.

</dd> <dt>

*cbResponse* \[ In\]
</dt> <dd>

Größe der Antwort in Bytes.

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

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





