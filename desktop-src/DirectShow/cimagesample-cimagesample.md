---
description: 'CImageSample.CImageSample-Konstruktor : Konstruktormethode.'
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
ms.openlocfilehash: 4eeb15ec42daed1fa835eff28a4953b223d9782859bfcc23b174dee8fee65019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402530"
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

## <a name="remarks"></a>Hinweise

Die [**CImageAllocator-Klasse**](cimageallocator.md) erstellt ein DIB mithilfe eines Dateizuordnungsobjekts, das von der Auslagerungsdatei des Betriebssystems unterstützt wird. Das Handle für das Dateizuordnungsobjekt wird im **hMapping-Member** der **m \_ DibData-Struktur** gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageSample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




