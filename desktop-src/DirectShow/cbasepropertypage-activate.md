---
description: Die Activate-Methode erstellt das Dialogfeldfenster. Diese Methode implementiert die IPropertyPage::Activate-Methode.
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: CBasePropertyPage.Activate-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b525eb16f534f0da8c847f50365c43124cb9e37d89f16629842fa202925a0674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108520"
---
# <a name="cbasepropertypageactivate-method"></a>CBasePropertyPage.Activate-Methode

Die `Activate` -Methode erstellt das Dialogfeldfenster. Diese Methode implementiert die **IPropertyPage::Activate-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* 
</dt> <dd>

Handle für das übergeordnete Fenster des Dialogfelds.

</dd> <dt>

*prect* 
</dt> <dd>

Zeiger auf eine **RECT-Struktur,** die Positionierungsinformationen für das Dialogfeld enthält.

</dd> <dt>

*fModal* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Dialogfeldrahmen modal (**TRUE**) oder moduslos ( FALSE )**ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                   | Beschreibung                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>       |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     |  NULL-Zeigerargument.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Unerwarteter Fehler.<br/>        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




