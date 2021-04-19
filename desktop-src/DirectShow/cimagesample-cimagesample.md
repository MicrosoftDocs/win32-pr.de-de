---
description: Konstruktormethode.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Cimagesample. cimagesample-Konstruktor (winutil. h)
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
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350786"
---
# <a name="cimagesamplecimagesample-constructor"></a>Cimagesample. cimagesample-Konstruktor

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

*pallocator* 
</dt> <dd>

Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.

</dd> <dt>

*pName* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*PHR* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer mit einer Größen *Länge*. Der Puffer sollte eine GDI-geräteunabhängige Bitmap (DIB) enthalten.

</dd> <dt>

*length* 
</dt> <dd>

Die Länge des Puffers.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Klasse [**cimagezuordcator**](cimageallocator.md) erstellt mithilfe eines Datei Zuordnungsobjekts, das von der Auslagerungs Datei des Betriebssystems unterstützt wird, ein DIB. Das Handle für das Datei Zuordnung-Objekt wird im **hmapping** -Member der **m \_ dibdata** -Struktur gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagesample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




