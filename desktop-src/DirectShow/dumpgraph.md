---
description: Die dumpgraph-Funktion sendet Informationen über ein Filter Diagramm an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Dumpgraph-Funktion (wxdebug. h)
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
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358606"
---
# <a name="dumpgraph-function"></a>Dumpgraph-Funktion

Die- `DumpGraph` Funktion sendet Informationen über ein Filter Diagramm an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PGraph* 
</dt> <dd>

Zeiger auf die [**ifiltergraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) -Schnittstelle im Filter Diagramm-Manager.

</dd> <dt>

*dwlevel* 
</dt> <dd>

Protokolliergrad. Die Funktion generiert eine Protokoll \_ Ablaufverfolgungs-Nachricht mit dem angegebenen Protokolliergrad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




