---
title: StreamSelectOperation.GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von SelectBestStreamAsync gestartet wurde.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- 'GetResults-Methode: Media Streaming-API'
- 'GetResults-Methode: Media Streaming-API, StreamSelectOperation-Schnittstelle'
- StreamSelectOperation-Schnittstelle Medienstreaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 022e75a57b9b38cff2a1e477d78a164767ab8cbcd4e1d3a159e8f61c8972fb95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952480"
---
# <a name="streamselectoperationgetresults-method"></a>StreamSelectOperation.GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**SelectBestStreamAsync gestartet wurde.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

