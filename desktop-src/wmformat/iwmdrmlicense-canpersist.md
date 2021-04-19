---
title: Iwmdrmlicense canpersistent-Methode (wmdrmsdk. h)
description: Die canpersistent-Methode fragt ab, ob die Lizenz in einem lokalen Lizenz Speicher persistent gespeichert werden kann.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Canpersistent-Methode Windows Media-Format
- Canpersistent-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, canpersistent-Methode
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
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354194"
---
# <a name="iwmdrmlicensecanpersist-method"></a>Iwmdrmlicense:: canpersistent-Methode

Die **canpersistent** -Methode fragt ab, ob die Lizenz in einem lokalen Lizenz Speicher persistent gespeichert werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfcanpersistent* \[ vorgenommen\]
</dt> <dd>

TRUE gibt an, dass die Lizenz beibehalten werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





