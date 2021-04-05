---
title: Ibasicdevice FriendlyName-Methode
description: Ruft den anzeigen amen des Geräts ab.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- FriendlyName-Methode Medien Streaming-API
- FriendlyName-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, FriendlyName-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718564"
---
# <a name="ibasicdevicefriendlyname-method"></a>Ibasicdevice:: FriendlyName-Methode

Ruft den anzeigen amen des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf den anzeigen amen des Geräts.

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

 

 





