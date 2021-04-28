---
description: CBasePropertyPage.CBasePropertyPage-Konstruktor – Konstruktormethode.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: CBasePropertyPage.CBasePropertyPage-Konstruktor (Cprop.h)
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
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119948"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>CBasePropertyPage.CBasePropertyPage-Konstruktor

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

Zeichenfolge, die den Namen des Objekts zu Debugzwecken enthält. Weitere Informationen finden Sie unter [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die aggregierende **IUnknown-Schnittstelle.**

</dd> <dt>

*DialogId* 
</dt> <dd>

Ressourcen-ID für das Dialogfeld.

</dd> <dt>

*TitleId* 
</dt> <dd>

Ressourcen-ID für die Zeichenfolge, die den Titel des Dialogfelds enthält.

</dd> </dl>

## <a name="examples"></a>Beispiele


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




