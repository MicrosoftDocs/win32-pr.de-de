---
title: Iwmdrmlicense reantenumeration-Methode (wmdrmsdk. h)
description: Die resetenumeration-Methode setzt die Lizenz Liste auf ihren ursprünglichen Zustand zurück. Die aktive Lizenz wird zur ersten Lizenz in der Liste.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Resegtenumeration-Methode Windows Media-Format
- Resegtenumeration-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, rerentenumeration-Methode
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
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367645"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>Iwmdrmlicense:: resstenumeration-Methode

Die **resetenumeration** -Methode setzt die Lizenz Liste auf ihren ursprünglichen Zustand zurück. Die aktive Lizenz wird zur ersten Lizenz in der Liste.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt> </dl> | Es wird eine aktualisierte Inhalts Sperr Liste benötigt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





