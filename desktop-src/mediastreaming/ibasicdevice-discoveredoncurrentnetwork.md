---
title: IBasicDevice DiscoveredOnCurrentNetwork-Methode
description: Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- 'DiscoveredOnCurrentNetwork-Methode: Medienstreaming-API'
- DiscoveredOnCurrentNetwork-Methode Media Streaming-API , IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , DiscoveredOnCurrentNetwork-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 605962315e4eab2cdbd5beab264747d282d78ef7c6f44b3bbcbf2f249bac7548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473489"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>IBasicDevice::D iscoveredOnCurrentNetwork-Methode

Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf einen booleschen Wert, der **True** ist, wenn sich das Gerät im aktuellen Netzwerk befindet.

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

 

 





