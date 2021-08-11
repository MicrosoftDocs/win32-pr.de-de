---
title: PlaybackOperation.GetResults-Methode
description: Gibt die Ergebnisse eines asynchronen Vorgangs zurück, der von einer der MediaRenderer-Wiedergabemethoden gestartet wurde.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- 'GetResults-Methode: Media Streaming-API'
- 'GetResults-Methode: Media Streaming-API, PlaybackOperation-Schnittstelle'
- PlaybackOperation-Schnittstelle Medienstreaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd3c79164a78e7993eb8a58d0d89a64c7ceb31a0c33eaff2e9c1bc352144088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235783"
---
# <a name="playbackoperationgetresults-method"></a>PlaybackOperation.GetResults-Methode

Gibt die Ergebnisse eines asynchronen Vorgangs zurück, der von einer der [**MediaRenderer-Wiedergabemethoden**](mediarenderer.md) gestartet wurde.

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

Das Ergebnis des Vorgangs. Der Wert 0 gibt an, dass der Vorgang abgeschlossen wurde. Andere Werte sind reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **GetResults-Methode** wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**Completed-Eigenschaft registriert**](playbackoperation-completed.md) wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





