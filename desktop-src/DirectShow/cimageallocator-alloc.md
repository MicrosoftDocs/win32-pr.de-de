---
description: 'Die Methode "Zuweisung" weist Speicher für die Puffer zu. Diese Methode überschreibt die cbasezucator:: Zuordnungsmethode.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Cimagezuzuordcator. Zuordnungsmethode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361564"
---
# <a name="cimageallocatoralloc-method"></a>Cimagezuzuordcator. Zuordnungsmethode

Die- `Alloc` Methode weist Speicher für die Puffer zu. Diese Methode überschreibt die [**cbasezucator:: Zuordnungsmethode**](cbaseallocator-alloc.md) .

## <a name="syntax"></a>Syntax


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                   | Beschreibung                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>             |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen, wenn der Filter einen Commit für die Zuweisung ausführt.

Diese Methode erstellt eine Liste von Medien Beispielen, die als [**cimagesample**](cimagesample.md) -Objekte implementiert werden. Jedes Beispiel enthält eine GDI-geräteunabhängige Bitmap, die die GDI-Funktion " **foratedibsection** " verwendet.

Intern ruft diese Methode [**cimagezuordcator:: kreatedib**](cimageallocator-createdib.md) auf, um jedes DIB zu erstellen, und [**cimagezuordcator:: forateimagesample**](cimageallocator-createimagesample.md) , um die einzelnen Beispiele zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagezuordcator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




