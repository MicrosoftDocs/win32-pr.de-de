---
title: Gettransportinformationoperation GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von gettransportinformationasync gestartet wurde.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, gettransportinformationoperation-Schnittstelle
- Gettransportinformationoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390260"
---
# <a name="gettransportinformationoperationgetresults-method"></a>Gettransportinformationoperation:: GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**gettransportinformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Ein Verweis auf eine [**Transportinformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) -Struktur, die die Ergebnisse des Vorgangs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](gettransportinformationoperation-completed.md) Eigenschaft registriert wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Gettransportinformationoperation**](gettransportinformationoperation.md)
</dt> </dl>

 

