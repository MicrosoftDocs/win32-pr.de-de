---
description: Die SetPalette-Methode installiert eine Palette für das Fenster. Diese Methode hat keine Parameter.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: CBaseWindow.SetPalette-Methode (Winutil.h) – Keine Parameter
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
ms.openlocfilehash: f15df65f6e427e467c14654a0e2745b84d774a5226b9a526193fc546261c5a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052150"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>CBaseWindow.SetPalette-Methode (Winutil.h) – Keine Parameter

Die `SetPalette` -Methode installiert eine Palette für das Fenster.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Ein interner Aufruf von **GdiFlush hat** einen Fehler zurückgegeben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Die palette, die von der [**CBaseWindow::m \_ hPalette-Membervariablen**](cbasewindow-m-hpalette.md) angegeben wird, wird ausgewählt. Der Aufrufer muss die Gültigkeit von **m \_ hPalette sicherstellen.**

Wenn der Wert der [**CBaseWindow::m \_ bNoRealize-Membervariable**](cbasewindow-m-bnorealize.md) **FALSE** (Standardeinstellung) ist, wählt diese Methode die Palette aus und erkennt sie. Andernfalls wird die Palette ausgewählt, aber nicht erkannt. Das -Objekt löscht keine vorherige Palette, die es verwendet hat. Der Aufrufer ist für das Löschen von Paletten verantwortlich.

Jeder Thread kann diese Methode sicher aufrufen, nicht nur den Thread, der das Fenster besitzt. Das Fenster sendet eine private Nachricht an sich selbst, die einen Aufruf der [**CBaseWindow::OnPaletteChange-Methode**](cbasewindow-onpalettechange.md) auslöst.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Winutil.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Einzelhandels-Builds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




