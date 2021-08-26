---
description: Die GetVideoPaletteEntries-Methode ruft einen Bereich von Paletteneinträgen für das Video ab.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: CBaseControlVideo.GetVideoPaletteEntries-Methode (Ctlutil.h)
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
ms.openlocfilehash: 5eb1c017353ed3e5095f5ee5d24870773c11211c14eaa44a673b4f12913c56c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057040"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>CBaseControlVideo.GetVideoPaletteEntries-Methode

Die `GetVideoPaletteEntries` -Methode ruft einen Bereich von Paletteneinträgen für das Video ab.

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

*Startindex* 
</dt> <dd>

Nullbasierter Startpaletteneintrag.

</dd> <dt>

*Einträge* 
</dt> <dd>

Anzahl der erforderlichen Einträge.

</dd> <dt>

*pRetrieved* 
</dt> <dd>

Zeiger auf die Anzahl der erhaltenen Farben.

</dd> <dt>

*pPalette* 
</dt> <dd>

Zeiger auf den Ausgabepuffer für Farben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück, wenn erfolgreich, VFW E NO PALETTE AVAILABLE, wenn die Videobeispiele keine Farbpalette \_ \_ \_ \_ haben, E \_ OUTOFMEMORY, \_  wenn nicht genügend Arbeitsspeicher verfügbar ist, E INVALIDARG, wenn StartIndex ungültig ist, oder S \_ FALSE, wenn keine Farben in der Palette vorhanden sind.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion gibt die aktuelle Palette des Videos als vom Benutzer zugeordnetes Array zurück. Um konsistent zu bleiben, verwenden Sie die Member in der Win32 **PALETTEENTRY-Struktur,** um die Farben zurückgibt, anstatt die Member in der **RGBQUAD-Struktur** (obwohl der -Parameter ein **LONG-Wert ist).** Der Arbeitsspeicher wird vom Aufrufer zugeordnet, also kopieren Sie einfach jeden nacheinander. Bestimmen Sie, ob die Anzahl der angeforderten Einträge und der Offset der Startposition gültig sind. Wenn die Anzahl der Einträge null ist, geben Sie einen S \_ FALSE-Code zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




