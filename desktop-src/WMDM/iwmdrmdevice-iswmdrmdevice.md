---
title: IWMDRMDevice IsWMDRMDevice-Methode
description: Die IsWMDRMDevice-Methode bestimmt, ob das Gerät Windows Media DRM 10 für portable Geräte unterstützt.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- IsWMDRMDevice-Methode windows Media Geräte-Manager
- IsWMDRMDevice-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice interface windows Media Geräte-Manager , IsWMDRMDevice method
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ee225267ce2301e9a2dad392d72ce72b0e698872cd3fd54ab3e50a07043477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957260"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>IWMDRMDevice::IsWMDRMDevice-Methode

Die **IsWMDRMDevice-Methode** bestimmt, ob das Gerät Windows Media DRM 10 für portable Geräte unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwVersion* \[ out\]
</dt> <dd>

Version von Windows Media DRM 10 für portable Geräte, die den Wert 0x00010000.

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

 

 





