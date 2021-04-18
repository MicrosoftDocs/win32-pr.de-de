---
title: Iwmdrmdevice iswmdrmdevice-Methode
description: Die iswmdrmdevice-Methode bestimmt, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Iswmdrmdevice-Methode, Windows Media Device Manager
- Iswmdrmdevice-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, iswmdrmdevice-Methode
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
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364926"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>Iwmdrmdevice:: iswmdrmdevice-Methode

Die **iswmdrmdevice** -Methode bestimmt, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwversion* \[ vorgenommen\]
</dt> <dd>

Version von Windows Media DRM 10 für tragbare Geräte, die den Wert 0x00010000 bis haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmddrmsp. idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





