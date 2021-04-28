---
description: 'CSourceStream.CSourceStream-Konstruktor : Konstruktormethode.'
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
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085188"
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

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert vor dem Erstellen des -Objekts mit S \_ OK. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*Pms* 
</dt> <dd>

Zeiger auf den [**CSource-Filter,**](csource.md) der diese Stecknadel erstellt hat.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen der Stecknadel enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die im *pObjectName-Parameter* angegebene Zeichenfolge wird nur zu Debugzwecken verwendet. Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)

Die im *pName-Parameter* angegebene Zeichenfolge ist der Name, der von der [**IPin::QueryPinInfo-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) zurückgegeben wird. Die `CSourceStream` -Klasse verwendet diesen Namen nicht für den pin-Bezeichner, der von der [**CSourceStream::QueryId-Methode**](csourcestream-queryid.md) zurückgegeben wird. Stattdessen berechnet **QueryId** einen Pinbezeichner basierend auf der Pinnummer. (Stecknadelbezeichner unterstützen die Graphpersistenz. Weitere Informationen finden Sie unter [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)

Der Konstruktor fügt den Pin automatisch dem besitzenden Filter hinzu, indem er [**CSource::AddPin aufruft.**](csource-addpin.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




