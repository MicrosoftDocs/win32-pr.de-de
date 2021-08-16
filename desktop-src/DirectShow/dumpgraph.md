---
description: Die DumpGraph-Funktion sendet Informationen zu einem Filterdiagramm an den Debugausgabespeicherort. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: DumpGraph-Funktion (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac09cc3381ab1b5f85f523d1c822768b3e2f87b6bcf08f1877680349072c216
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820959"
---
# <a name="dumpgraph-function"></a>DumpGraph-Funktion

Die `DumpGraph` Funktion sendet Informationen zu einem Filterdiagramm an den Debugausgabespeicherort. Wird in Einzelhandelsbuilds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGraph* 
</dt> <dd>

Zeiger auf die [**IFilterGraph-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) im Filtergraph-Manager.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Protokolliergrad. Die Funktion generiert eine LOG \_ TRACE-Nachricht mit dem angegebenen Protokolliergrad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debuggen von Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




