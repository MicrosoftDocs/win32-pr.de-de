---
title: IWMDRMLicense ResetEnumeration-Methode (Wmdrmsdk.h)
description: Die ResetEnumeration-Methode setzt die Lizenzliste auf ihren ursprünglichen Zustand zurück. Die aktive Lizenz wird zur ersten Lizenz in der Liste.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- ResetEnumeration-Methode – Windows-Medienformat
- ResetEnumeration-Methode Windows Media Format, IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle Windows Media Format , ResetEnumeration-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6de46a2ce96d1fec1abaaae56edcbc5b0d6a73e8ee13f038dba6b5577c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027688"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>IWMDRMLicense::ResetEnumeration-Methode

Die **ResetEnumeration-Methode** setzt die Lizenzliste auf ihren ursprünglichen Zustand zurück. Die aktive Lizenz wird zur ersten Lizenz in der Liste.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ \_ DRM:NS: ZU \_ \_ KLEIN**</dt> </dl> | Eine aktualisierte Inhaltssperrliste ist erforderlich.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





