---
description: 'CImageSample.CImageSample-Konstruktor: Konstruktormethode.'
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: CImageSample.CImageSample-Konstruktor (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095608"
---
# <a name="cimagesamplecimagesample-constructor"></a>CImageSample.CImageSample-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAllocator* 
</dt> <dd>

Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.

</dd> <dt>

*pName* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer der *Größe*. Der Puffer sollte eine geräteunabhängige GDI-Bitmap (DIB) enthalten.

</dd> <dt>

*length* 
</dt> <dd>

Die Länge des Puffers.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**CImageAllocator-Klasse**](cimageallocator.md) erstellt einen DIB mithilfe eines Dateizuordnungsobjekts, das von der Auslagerungsdatei des Betriebssystems erstellt wird. Das Handle für das Dateizuordnungsobjekt wird im **hMapping-Member** der **m \_ DibData-Struktur** gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageSample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




