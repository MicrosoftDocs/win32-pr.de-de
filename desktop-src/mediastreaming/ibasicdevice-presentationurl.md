---
title: IBasicDevice PresentationUrl-Methode
description: Ruft die Präsentations-URL des Geräts ab.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- 'PresentationUrl-Methode: Media Streaming-API'
- 'PresentationUrl-Methode: Media Streaming-API, IBasicDevice-Schnittstelle'
- IBasicDevice-Schnittstelle Medienstreaming-API, PresentationUrl-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d5908b80e7b413ca646279a751e12ec7d9c7e6e98ae7ecff3ad1f1d9e60bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235937"
---
# <a name="ibasicdevicepresentationurl-method"></a>IBasicDevice::P resentationUrl-Methode

Ruft die Präsentations-URL des Geräts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die Präsentations-URL des Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





