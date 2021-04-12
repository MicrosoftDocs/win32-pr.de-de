---
title: Getstreampropertiesoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getstreampropertiesasync gestartet wurde.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getstreampropertiesoperation-Schnittstelle
- Getstreampropertiesoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390235"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>Getstreampropertiesoperation. GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getstreampropertiesasync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))gestartet wurde.

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

[**Getstreampropertiesoperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

