---
title: IWMDRMLicense CanPersist-Methode (Wmdrmsdk.h)
description: Die CanPersist-Methode fragt ab, ob die Lizenz in einem lokalen Lizenzspeicher beibehalten werden kann.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- 'CanPersist-Methode : Windows-Medienformat'
- CanPersist-Methode windows Media Format, IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle Windows Media Format , CanPersist-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e174f0b7d48684e40cc5796d2ae95ec1bcaca99216c493c73609323daf276b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701218"
---
# <a name="iwmdrmlicensecanpersist-method"></a>IWMDRMLicense::CanPersist-Methode

Die **CanPersist-Methode** fragt ab, ob die Lizenz in einem lokalen Lizenzspeicher beibehalten werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfCanPersist* \[ out\]
</dt> <dd>

TRUE gibt an, dass die Lizenz beibehalten werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





