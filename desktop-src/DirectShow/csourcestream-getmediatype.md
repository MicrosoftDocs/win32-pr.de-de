---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp ab. Diese Methode verwendet die Parameter *iPosition* und *pmediatype* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Csourcestream. getmediatype-Methode (Source. h)-iPosition-und pmediatype-Parameter
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372538"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>Csourcestream. getmediatype-Methode (Source. h)-iPosition-und pmediatype-Parameter

Die **getmediatype** -Methode ruft einen bevorzugten Medientyp ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPosition* 
</dt> <dd>

NULL basierter Indexwert.

</dd> <dt>

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
| Header  | Source. h (Include Streams. h)                                                                                    |
| Bibliothek | "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




