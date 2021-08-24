---
title: GetPositionInformationOperation.GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von GetPositionInformationAsync gestartet wurde.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- 'GetResults-Methode: Media Streaming-API'
- 'GetResults-Methode: Media Streaming-API, GetPositionInformationOperation-Schnittstelle'
- GetPositionInformationOperation-Schnittstelle Media Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e924227c37318a788f9c30aea5e5125a40c69175ac7c4449a54ebcc4cf61326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721060"
---
# <a name="getpositioninformationoperationgetresults-method"></a>GetPositionInformationOperation.GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**GetPositionInformationAsync gestartet wurde.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Ein Verweis auf eine [**PositionInformation-Struktur,**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) die die Ergebnisse des Vorgangs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **GetResults-Methode** wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**Completed-Eigenschaft registriert**](getpositioninformationoperation-completed.md) wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

