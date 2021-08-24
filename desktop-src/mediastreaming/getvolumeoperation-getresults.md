---
title: GetVolumeOperation.GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von GetVolumeAsync gestartet wurde.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- 'GetResults-Methode: Media Streaming-API'
- 'GetResults-Methode: Media Streaming-API, GetVolumeOperation-Schnittstelle'
- GetVolumeOperation-Schnittstelle Medienstreaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e58188a0d8b0d2ed13a9cb7d7486f440f4a1303ca32208371690965f976339d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011850"
---
# <a name="getvolumeoperationgetresults-method"></a>GetVolumeOperation.GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**GetVolumeAsync gestartet wurde.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Das Volume. Ein Wert zwischen 0 und 100. 0 gibt das mindeste Volumen und 100 das maximale Volume an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **GetResults-Methode** wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**Completed-Eigenschaft registriert**](getvolumeoperation-completed.md) wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

