---
description: Die Apply-Methode wendet die aktuellen Eigenschaftsseitenwerte auf das Objekt an, das der Eigenschaftenseite zugeordnet ist. Diese Methode implementiert die IPropertyPage::Apply-Methode.
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: CBasePropertyPage.Apply-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9350aa7aaa4e2bfdcb72385d26b09b9d7a9bdf33deb05e273b0663485da1a5bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823233"
---
# <a name="cbasepropertypageapply-method"></a>CBasePropertyPage.Apply-Methode

Die `Apply` -Methode wendet die aktuellen Eigenschaftsseitenwerte auf das -Objekt an, das der Eigenschaftenseite zugeordnet ist. Diese Methode implementiert die **IPropertyPage::Apply-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn das [**CBasePropertyPage::m \_ bDirty-Flag**](cbasepropertypage-m-bdirty.md) **TRUE** ist, ruft diese Methode die [**CBasePropertyPage::OnApplyChanges-Methode auf.**](cbasepropertypage-onapplychanges.md) Überschreiben Sie **OnApplyChanges,** um die Änderungen auf das -Objekt anzuwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




