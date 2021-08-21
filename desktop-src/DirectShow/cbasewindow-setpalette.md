---
description: Die SetPalette-Methode installiert eine Palette für das Fenster.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: CBaseWindow.SetPalette-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c04d4e24c621dd704b8aeba91646016e334a6f6bface4769578a710322a7cff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074554"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>CBaseWindow.SetPalette-Methode (Winutil.h)

Die `SetPalette` -Methode installiert eine Palette für das Fenster.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPalette* 
</dt> <dd>

Handle für die neue Palette. Darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Ein interner Aufruf von **GdiFlush** hat einen Fehler zurückgegeben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Wenn der Wert der [**CBaseWindow::m \_ bNoRealize-Membervariable**](cbasewindow-m-bnorealize.md) **FALSE** ist (Standardeinstellung), wählt diese Methode die Palette aus und erkennt sie. Andernfalls wird die Palette ausgewählt, aber nicht erkannt. Das -Objekt löscht keine vorherige Palette, die es verwendet hat. Der Aufrufer ist für das Löschen von Paletten verantwortlich.

Jeder Thread kann diese Methode sicher aufrufen, nicht nur den Thread, der das Fenster besitzt. Das Fenster sendet eine private Nachricht an sich selbst, wodurch ein Aufruf der [**CBaseWindow::OnPaletteChange-Methode**](cbasewindow-onpalettechange.md) ausgelöst wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




