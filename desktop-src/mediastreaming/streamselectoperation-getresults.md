---
title: Streamselectoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von selectbeststreamasync gestartet wurde.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, streamselectoperation-Schnittstelle
- Streamselectoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106342124"
---
# <a name="streamselectoperationgetresults-method"></a>Streamselectoperation. GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**selectbeststreamasync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ Out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Streamselectoperation**](streamselectoperation.md)
</dt> </dl>

 

