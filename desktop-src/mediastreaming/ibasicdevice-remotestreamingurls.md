---
title: IBasicDevice RemoteStreamingUrls-Methode
description: Gibt einen Vektor von Remotestreaming-URLs zurück.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- RemoteStreamingUrls-Methode Media Streaming-API
- 'RemoteStreamingUrls-Methode: Media Streaming-API, IBasicDevice-Schnittstelle'
- IBasicDevice-Schnittstelle Medienstreaming-API, RemoteStreamingUrls-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d98d908cb582c0c2885a9b24a0a525f1e719c82bdffe20e74597ca5fc262a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972329"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>IBasicDevice::RemoteStreamingUrls-Methode

Gibt einen Vektor von Remotestreaming-URLs zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt eine aufzählbare Auflistung von Zeigern auf Remotestreaming-URLs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





