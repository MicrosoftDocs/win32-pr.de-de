---
description: 'CSourceStream.CSourceStream-Konstruktor: Konstruktormethode.'
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: CSourceStream.CSourceStream-Konstruktor (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e02827c74ef4c5461a5777221e1839846b855a4b2f4cd27d97ce913399787ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053850"
---
# <a name="csourcestreamcsourcestream-constructor"></a>CSourceStream.CSourceStream-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Debugnamen des Pins enthält.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*Pms* 
</dt> <dd>

Zeiger auf den [**CSource-Filter,**](csource.md) der diesen Pin erstellt hat.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen der Stecknadel enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die im *pObjectName-Parameter angegebenen* Zeichenfolgen werden nur zu Debugzwecken verwendet. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

Die im *pName-Parameter übergebene Zeichenfolge* ist der Von der [**IPin::QueryPinInfo-Methode zurückgegebene**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Name. Die `CSourceStream` -Klasse verwendet diesen Namen nicht für den Pinbezeichner, der von der [**CSourceStream::QueryId-Methode zurückgegeben**](csourcestream-queryid.md) wird. Stattdessen berechnet **QueryId** einen Pinbezeichner basierend auf der Pinnummer. (Pinbezeichner unterstützen Graphpersistenz. Weitere Informationen finden Sie unter [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)

Der Konstruktor fügt den Pin automatisch dem besitzenden Filter hinzu, indem er [**CSource::AddPin aufruft.**](csource-addpin.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




