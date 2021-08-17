---
title: GetTransportInformationOperation GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von GetTransportInformationAsync gestartet wurde.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- 'GetResults-Methode: Medienstreaming-API'
- 'GetResults-Methode: Medienstreaming-API, GetTransportInformationOperation-Schnittstelle'
- GetTransportInformationOperation-Schnittstelle Medienstreaming-API , GetResults-Methode
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbcc6345a09d0553df240c57e50b4498618be76cc75814f268892aa6e0b4dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100634"
---
# <a name="gettransportinformationoperationgetresults-method"></a>GetTransportInformationOperation::GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ out, retval\]
</dt> <dd>

Ein Verweis auf eine [**TransportInformation-Struktur,**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) die die Ergebnisse des Vorgangs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **GetResults-Methode** wird in der Regel über den Ereignishandler aufgerufen, der durch Festlegen der [**Completed-Eigenschaft**](gettransportinformationoperation-completed.md) registriert wurde.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

