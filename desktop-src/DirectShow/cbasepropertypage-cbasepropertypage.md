---
description: Konstruktormethode.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Cbasepropertypage. cbasepropertypage-Konstruktor (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359224"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Cbasepropertypage. cbasepropertypage-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Eine Zeichenfolge, die den Namen des Objekts zu Debuggingzwecken enthält. Weitere Informationen finden Sie unter [**cbaseobject:: cbaseobject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf die Aggregations- **IUnknown** -Schnittstelle.

</dd> <dt>

*DialogID* 
</dt> <dd>

Die Ressourcen-ID für das Dialogfeld.

</dd> <dt>

*TitleId* 
</dt> <dd>

Die Ressourcen-ID für die Zeichenfolge, die den Dialogfeld Titel enthält.

</dd> </dl>

## <a name="examples"></a>Beispiele


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




