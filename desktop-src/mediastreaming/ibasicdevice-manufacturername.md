---
title: Ibasicdevice ManufacturerName-Methode
description: Ruft den Herstellernamen des Geräts ab.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- ManufacturerName-Methode Medien Streaming-API
- ManufacturerName-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, ManufacturerName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340248"
---
# <a name="ibasicdevicemanufacturername-method"></a>Ibasicdevice:: ManufacturerName-Methode

Ruft den Herstellernamen des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf den Herstellernamen des Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibasicdevice**](ibasicdevice.md)
</dt> </dl>

 

 





