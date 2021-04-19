---
description: 'Die queryfilterinfo-Methode ruft Informationen über den Filter ab. Diese Methode implementiert die ibasefilter:: queryfilterinfo-Methode.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Cbasefilter. queryfilterinfo-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374021"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Cbasefilter. queryfilterinfo-Methode

Die- `QueryFilterInfo` Methode ruft Informationen über den Filter ab. Diese Methode implementiert die [**ibasefilter:: queryfilterinfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* 
</dt> <dd>

Zeiger auf eine [**Filter \_ Informations**](/windows/win32/api/strmif/ns-strmif-filter_info) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kopiert den Filternamen aus der [**cbasefilter:: m \_ PName**](cbasefilter-m-pname.md) -Element Variablen in den " **achname** "-Member der Filter \_ Informationsstruktur. Wenn **m \_ PName** **null** ist, legt die Methode " **achname** " auf L " \\ 0" fest.

Die-Methode legt den **PGraph** -Member der Filter \_ Info-Struktur gleich der [**cbasefilter:: m \_ PGraph**](cbasefilter-m-pgraph.md) -Element Variablen fest und erhöht den Verweis Zähler. Der Aufrufer muss die-Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




