---
title: Imediarendereraktioninformation isvolumeavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR die audiovolumeebene anpassen kann.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- Isvolumeavailable-Methode Medien Streaming-API
- Isvolumeavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isvolumeavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101510"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a>Imediarendereraktioninformation:: isvolumeavailable-Methode

Ruft einen Wert ab, der angibt, ob der DMR die audiovolumeebene anpassen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR die audiovolumeebene anpassen kann, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

