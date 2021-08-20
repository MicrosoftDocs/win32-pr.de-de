---
description: Die SetObjects-Methode stellt IUnknown-Zeiger für die Objekte bereit, die der Eigenschaftenseite zugeordnet sind. Diese Methode implementiert die IPropertyPage::SetObjects-Methode.
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: CBasePropertyPage.SetObjects-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e5c29d1ddc646ef05faad2bc283887265e8b85109fcb679924d9a5641ef13fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823025"
---
# <a name="cbasepropertypagesetobjects-method"></a>CBasePropertyPage.SetObjects-Methode

Die `SetObjects` -Methode stellt **IUnknown-Zeiger** für die Objekte bereit, die der Eigenschaftenseite zugeordnet sind. Diese Methode implementiert die **IPropertyPage::SetObjects-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cObjects* 
</dt> <dd>

Gibt die Anzahl der **IUnknown-Zeiger** im array an, das von *ppUnk* angegeben wird.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Gibt ein Array von **IUnknown-Zeigern** an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                   |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | **NULL-Zeigerargument.**<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler.<br/>        |



 

## <a name="remarks"></a>Hinweise

Obwohl *ppUnk* ein Array von **IUnknown-Zeigern** angibt, ist die **CBasePropertyPage-Klasse** nur für die Unterstützung eines zugeordneten Objekts konzipiert. Wenn *cObjects* größer als 1 ist, gibt die Methode E \_ UNEXPECTED zurück.

Wenn *cObjects* gleich 1 ist, ruft diese Methode die [**CBasePropertyPage::OnConnect-Methode auf.**](cbasepropertypage-onconnect.md) Wenn *cObjects* gleich 0 ist, ruft diese Methode die [**CBasePropertyPage::OnDisconnect-Methode auf.**](cbasepropertypage-ondisconnect.md) Die abgeleitete Klasse sollte beide Methoden überschreiben. Weitere Informationen finden Sie in den Hinweisen zu diesen Methoden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




