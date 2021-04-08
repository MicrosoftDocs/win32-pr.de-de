---
title: Getpositioninformationoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getpositioninformationasync gestartet wurde.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getpositioninformationoperation-Schnittstelle
- Getpositioninformationoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726760"
---
# <a name="getpositioninformationoperationgetresults-method"></a>Getpositioninformationoperation. GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Ein Verweis auf eine [**positioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) -Struktur, die die Ergebnisse des Vorgangs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](getpositioninformationoperation-completed.md) Eigenschaft registriert wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getpositioninformationoperation**](getpositioninformationoperation.md)
</dt> </dl>

 

