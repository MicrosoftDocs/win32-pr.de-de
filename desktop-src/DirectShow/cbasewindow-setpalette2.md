---
description: Die SetPalette-Methode installiert eine Palette für das Fenster. Diese Methode hat keine Parameter.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Cbasewindow. SetPalette-Methode (winutil. h)-keine Parameter
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
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219730"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Cbasewindow. SetPalette-Methode (winutil. h)-keine Parameter

Mit der- `SetPalette` Methode wird eine Palette für das-Fenster installiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Ein interner-Befehl von " **gdiflush** " hat einen Fehler zurückgegeben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Die von der [**cbasewindow:: m \_ hpalette**](cbasewindow-m-hpalette.md) -Member-Variable angegebene Palette ist ausgewählt. Der Aufrufer muss die Gültigkeit von **m \_ hpalette** sicherstellen.

Wenn der Wert der [**cbasewindow:: m \_ bnorealize**](cbasewindow-m-bnorealize.md) -Element Variablen **false** (Standardeinstellung) ist, wählt diese Methode die Palette aus und erkennt Sie. Andernfalls wird die Palette ausgewählt, aber nicht erkannt. Das Objekt löscht keine zuvor verwendete Palette. Der Aufrufer ist für das Löschen von Paletten verantwortlich.

Jeder Thread kann diese Methode sicher aufzurufen, nicht nur den Thread, der das Fenster besitzt. Das Fenster sendet eine private Nachricht an sich selbst, wodurch ein Aufrufvorgang der [**cbasewindow:: onpalettechange**](cbasewindow-onpalettechange.md) -Methode ausgelöst wird.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Winutil. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




