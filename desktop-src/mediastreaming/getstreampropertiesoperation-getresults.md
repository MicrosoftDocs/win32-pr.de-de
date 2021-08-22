---
title: GetStreamPropertiesOperation.GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von GetStreamPropertiesAsync gestartet wurde.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- 'GetResults-Methode: Media Streaming-API'
- 'GetResults-Methode: Media Streaming-API, GetStreamPropertiesOperation-Schnittstelle'
- GetStreamPropertiesOperation-Schnittstelle Media Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3520cc44919e9c606c6625c75193b5f1ab54f4005cc098316bd8769ad0e0fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735821"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>GetStreamPropertiesOperation.GetResults-Methode

Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**GetStreamPropertiesAsync gestartet wurde.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

