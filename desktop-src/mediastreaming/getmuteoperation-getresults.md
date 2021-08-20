---
title: GetMuteOperation.GetResults-Methode
description: Gibt die Ergebnisse des von GetMuteAsync gestarteten asynchronen Vorgangs zurück.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- 'GetResults-Methode: Medienstreaming-API'
- 'GetResults-Methode: Medienstreaming-API, GetMuteOperation-Schnittstelle'
- GetMuteOperation-Schnittstelle Medienstreaming-API , GetResults-Methode
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37b8356a677f5e752fdf4e4ec658cc4077a17fa76b6181097d5753d898eef89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972409"
---
# <a name="getmuteoperationgetresults-method"></a>GetMuteOperation.GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out, retval\]
</dt> <dd>

Der Stummschaltungswert. Der Wert true gibt an, dass audio derzeit stummgeschaltet ist. Der Wert false gibt an, dass audio nicht stummgeschaltet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **GetResults-Methode** wird in der Regel über den Ereignishandler aufgerufen, der durch Festlegen der [**Completed-Eigenschaft**](getmuteoperation-completed.md) registriert wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

