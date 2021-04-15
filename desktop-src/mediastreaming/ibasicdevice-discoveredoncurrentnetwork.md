---
title: Ibasicdevice discoveredoncurrentnetwork-Methode
description: Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- Discoveredoncurrentnetwork-Methode Medien Streaming-API
- Discoveredoncurrentnetwork-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, discoveredoncurrentnetwork-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389047"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>Ibasicdevice::D iscoveredoncurrentnetwork-Methode

Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf einen booleschen Wert, der **true** ist, wenn sich das Gerät im aktuellen Netzwerk befindet.

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

 

 





