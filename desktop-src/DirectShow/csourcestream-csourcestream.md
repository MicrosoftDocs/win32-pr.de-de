---
description: Konstruktormethode.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Csourcestream. csourcestream-Konstruktor (Source. h)
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
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358048"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Csourcestream. csourcestream-Konstruktor

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

*pobjectname* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den debugnamen der PIN enthält.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist. Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*PMS* 
</dt> <dd>

Zeiger auf den [**CSource**](csource.md) -Filter, der diese Pin erstellt hat.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen der PIN enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die im *pobjectname* -Parameter angegebene Zeichenfolge wird nur für Debugzwecke verwendet. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

Die im *PName* -Parameter angegebene Zeichenfolge ist der Name, der von der [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) -Methode zurückgegeben wird. Die- `CSourceStream` Klasse verwendet diesen Namen nicht für den PIN-Bezeichner, der von der [**csourcestream:: QueryId**](csourcestream-queryid.md) -Methode zurückgegeben wird. Stattdessen berechnet **QueryId** einen PIN-Bezeichner basierend auf der PIN-Nummer. (PIN-Bezeichner unterstützen die Diagramm Persistenz. Weitere Informationen finden Sie unter [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)

Der Konstruktor fügt die PIN automatisch dem besitzenden Filter hinzu, indem [**CSource:: addpin**](csource-addpin.md)aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




