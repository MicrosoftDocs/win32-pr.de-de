---
description: Die getvideopaletteentries-Methode ruft einen Bereich von paletteneinträgen für das Video ab.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Cbasecontrolvideo. getvideopaletteentries-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366866"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>Cbasecontrolvideo. getvideopaletteentries-Methode

Die- `GetVideoPaletteEntries` Methode ruft einen Bereich von paletteneinträgen für das Video ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start Index* 
</dt> <dd>

Der null basierte Start Paletteneintrag.

</dd> <dt>

*Gewinner* 
</dt> <dd>

Anzahl der erforderlichen Einträge.

</dd> <dt>

*vorab bereitgestellt* 
</dt> <dd>

Ein Zeiger auf die Anzahl der gewonnenen Farben.

</dd> <dt>

*pPalette* 
</dt> <dd>

Zeiger auf den Ausgabepuffer für Farben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt noError zurück, wenn nicht genügend Arbeitsspeicher verfügbar ist, Vfw \_ e \_ keine \_ Palette \_ verfügbar ist, wenn die Videobeispiele keine Farbpalette haben, e \_ OutOfMemory, wenn nicht genügend Arbeitsspeicher verfügbar ist, e \_ invalidArg if *startIndex* ist ungültig, oder S \_ false, wenn die Palette keine Farben enthält.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion gibt die aktuelle Palette des Videos als Array zurück, das vom Benutzer zugeordnet wird. Um konsistent zu bleiben, verwenden Sie die Elemente in der Win32 **PaletteEntry** -Struktur, um die Farben anstelle der Elemente in der **rgbquad** -Struktur zurückzugeben (obwohl der-Parameter ein **Long**-Parameter ist). Der Arbeitsspeicher wird vom Aufrufer zugeordnet. Kopieren Sie also alle nacheinander. Stellen Sie fest, dass die Anzahl der angeforderten Einträge und der Offset der Startposition gültig sind. Wenn die Anzahl der Einträge NULL ergibt, wird ein S false-Code zurückgegeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




