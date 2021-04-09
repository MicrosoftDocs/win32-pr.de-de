---
title: Getmuteoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getmuteasync gestartet wurde.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getmuteoperation-Schnittstelle
- Getmuteoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101514"
---
# <a name="getmuteoperationgetresults-method"></a>Getmuteoperation. GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getmuteasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd>

Der stumm Wert. Der Wert true gibt an, dass Audiodaten zurzeit stumm geschaltet werden. Der Wert false gibt an, dass Audiodaten nicht stumm geschaltet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **GetResults** -Methode wird in der Regel vom Ereignishandler aufgerufen, der durch Festlegen der [**abgeschlossenen**](getmuteoperation-completed.md) Eigenschaft registriert wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getmuteoperation**](getmuteoperation.md)
</dt> </dl>

 

