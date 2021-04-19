---
description: Die m \_ bmodifiesdata-Member-Variable gibt an, ob der Filter die Beispiel Daten ändert, die empfangen werden. Der Wert wird im ctransinplacefilter-Konstruktor festgelegt, jedoch ist der Standardwert true.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Ctransinplacefilter:: m_bModifiesData Member (transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361920"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Ctransinplacefilter:: m \_ bmodifiesdata-Member

Die `m_bModifiesData` Member-Variable gibt an, ob der Filter die Beispiel Daten ändert, die empfangen werden. Der Wert wird im **ctransinplacefilter** -Konstruktor festgelegt, jedoch ist der Standardwert **true**.

## <a name="syntax"></a>Syntax


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Bemerkungen

Diese Variable wirkt sich darauf aus, wie der Filter die Zuweisung aushandtert. Wenn der Wert **true** ist, kann der Filter keine schreibgeschützte Zuweisung für beide Pin-Verbindungen verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




