---
title: IWMDRMLicense PersistLicense-Methode (Wmdrmsdk.h)
description: Die PersistLicense-Methode speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenzspeicher.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- PersistLicense-Methode – Windows-Medienformat
- PersistLicense-Methode windows Media Format, IWMDRMLicense-Schnittstelle
- IWMDRMLicense interface windows Media Format , PersistLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2c002daefc7b4a27e3907ea6bc9faafc25c4c8d10862cc19518c719e2fb354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655138"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>IWMDRMLicense::P ersistLicense-Methode

Die **PersistLicense-Methode** speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenzspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn sich die aktuelle Lizenz nicht im temporären Speicher befindet, kann diese Methode nicht verwendet werden.

Sie können [**CanPersist aufrufen,**](iwmdrmlicense-canpersist.md) um zu fragen, ob die Lizenz beibehalten werden darf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





