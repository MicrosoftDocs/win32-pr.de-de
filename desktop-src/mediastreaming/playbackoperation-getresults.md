---
title: Playbackoperation. GetResults-Methode
description: Gibt die Ergebnisse eines asynchronen Vorgangs zurück, der von einer der MediaRenderer-Wiedergabe Methoden gestartet wurde.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, playbackoperation-Schnittstelle
- Playbackoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104388914"
---
# <a name="playbackoperationgetresults-method"></a>Playbackoperation. GetResults-Methode

Gibt die Ergebnisse eines asynchronen Vorgangs zurück, der von einer der [**MediaRenderer**](mediarenderer.md) -Wiedergabe Methoden gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Das Ergebnis des Vorgangs. Der Wert 0 gibt an, dass der Vorgang abgeschlossen wurde. Andere Werte sind reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](playbackoperation-completed.md) Eigenschaft registriert wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playbackoperation**](playbackoperation.md)
</dt> </dl>

 

 





