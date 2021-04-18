---
description: 'Die SetObjects-Methode stellt IUnknown-Zeiger für die Objekte bereit, die der Eigenschaften Seite zugeordnet sind. Diese Methode implementiert die IPropertyPage:: abtobjects-Methode.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Cbasepropertypage. * tobjects-Methode (cprop. h)
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
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368647"
---
# <a name="cbasepropertypagesetobjects-method"></a>Cbasepropertypage. * tobjects-Methode

Die- `SetObjects` Methode stellt **IUnknown** -Zeiger für die Objekte bereit, die der Eigenschaften Seite zugeordnet sind. Diese Methode implementiert die **IPropertyPage:: abtobjects** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*eines CObject* 
</dt> <dd>

Gibt die Anzahl der **IUnknown** -Zeiger in dem Array an, das von *ppUnk* angegeben wird.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Gibt ein Array von **IUnknown** -Zeigern an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Obwohl *ppUnk* ein Array von **IUnknown** -Zeigern angibt, ist die **cbasepropertypage** -Klasse nur für die Unterstützung eines zugeordneten Objekts vorgesehen. Wenn *CObjects* größer als 1 ist, gibt die Methode E \_ unerwartet zurück.

Wenn *CObjects* 1 ist, ruft diese Methode die [**cbasepropertypage:: OnConnect**](cbasepropertypage-onconnect.md) -Methode auf. Wenn *CObjects* 0 (null) ist, ruft diese Methode die [**cbasepropertypage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) -Methode auf. Die abgeleitete Klasse sollte beide Methoden überschreiben. Weitere Informationen finden Sie in den Hinweisen zu diesen Methoden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




