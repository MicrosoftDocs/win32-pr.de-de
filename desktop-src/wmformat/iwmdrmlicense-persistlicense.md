---
title: Iwmdrmlicense persistlicense-Methode (wmdrmsdk. h)
description: Die persistlicense-Methode speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenz Speicher.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Persistlicense-Methode Windows Media-Format
- Persistlicense-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, persistlicense-Methode
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
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370073"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>Iwmdrmlicense::P ersistlicense-Methode

Die **persistlicense** -Methode speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenz Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn sich die aktuelle Lizenz nicht im temporären Speicher befindet, schlägt diese Methode fehl.

Sie können [**canpersistent**](iwmdrmlicense-canpersist.md) aufzurufen, um abzufragen, ob die Lizenz beibehalten werden darf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





