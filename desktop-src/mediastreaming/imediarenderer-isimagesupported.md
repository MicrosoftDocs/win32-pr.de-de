---
title: Imediarenderer-Methode (isimagesupported)
description: Ruft einen Wert ab, der angibt, ob der DMR Bilder anzeigen kann.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- Isimagesupported-Methode Medien Streaming-API
- Isimagesupported-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, isimagesupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342101"
---
# <a name="imediarendererisimagesupported-method"></a>Imediarenderer:: isimagesupported-Methode

Ruft einen Wert ab, der angibt, ob der DMR Bilder anzeigen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein boolescher Wert, der **true** ist, wenn der DMR Bilder anzeigen kann, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediarenderer**](imediarenderer.md)
</dt> </dl>

 

 





