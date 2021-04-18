---
description: 'Die setpositions-Methode legt die aktuelle Position und die Position des Stopps fest. Diese Methode implementiert die imediaseeking:: setpositions-Methode.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Csourceseeking. setpositions-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357691"
---
# <a name="csourceseekingsetpositions-method"></a>Csourceseeking. setpositions-Methode

Die `SetPositions` -Methode legt die aktuelle Position und die Position des Stopps fest. Diese Methode implementiert die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrent* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Position angibt.

</dd> <dt>

*Currentflags* 
</dt> <dd>

Bitweise Kombination von-Flags. Siehe Hinweise.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats angibt.

</dd> <dt>

*Stopflags* 
</dt> <dd>

Bitweise Kombination von-Flags. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                  | Beschreibung                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültige Flags.<br/>             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Flags werden unterstützt:

-   \_Suchen von \_ noposior
-   \_Sucht nach \_ absolutepositionierung
-   \_Suche nach \_ relativepositionierung
-   \_ \_ Inkrementalpositionierung suchen (nur *Pend* )

Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Diese Methode aktualisiert die Werte der [**csourceseeking:: m \_ rtstart**](csourceseeking-m-rtstart.md) -und [**csourceseeking:: m \_ rtstoppt**](csourceseeking-m-rtstop.md) -Element Variablen und ruft dann die reinen virtuellen Methoden [**csourceseeking:: changestart**](csourceseeking-changestart.md) und [**csourceseeking:: changestoppt**](csourceseeking-changestop.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




