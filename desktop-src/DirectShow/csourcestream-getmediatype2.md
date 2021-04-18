---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp ab.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Csourcestream. getmediatype-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62d79faab8d48d748f4a2c787dd1cbc8f6d2ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372601"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Csourcestream. getmediatype-Methode (Quelle. h)

Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediatype* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt> </dl> | Der Index liegt außerhalb des zulässigen Bereichs.<br/>   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>           | Index kleiner als 0 (null).<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>           | Unerwarteter Fehler.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Es gibt zwei Versionen dieser Methode. Eine Version überschreibt die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode und übernimmt einen Indexwert als Parameter. Die andere Version dient zum Abrufen eines einzelnen Medientyps, sodass der Index-Parameter fehlt.

Die Methode mit einem Parameter gibt "E unerwartete" zurück \_ . Die zwei-Parameter-Methode überprüft, ob der *iPosition* -Parameter NULL ist, und ruft dann die Einzel Parameter Version auf. Abhängig von der Anzahl der Medientypen, die von der PIN unterstützt werden, müssen Sie eine dieser Methoden überschreiben:

-   Wenn die PIN genau einen Medientyp unterstützt, überschreiben Sie die Einzel Parameter Version. Füllen Sie den Medientyp aus, der von der PIN unterstützt wird.
-   Wenn die PIN mehr als einen Medientyp unterstützt, überschreiben Sie die Version mit zwei Parametern. Überschreiben Sie außerdem die [**csourcestream:: checkmediatype**](csourcestream-checkmediatype.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




