---
description: Die SetPalette-Methode installiert eine Palette für das Fenster.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Cbasewindow. SetPalette-Methode (winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369990"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>Cbasewindow. SetPalette-Methode (winutil. h)

Mit der- `SetPalette` Methode wird eine Palette für das-Fenster installiert.

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

Handle für die neue Palette. Darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Ein interner-Befehl von " **gdiflush** " hat einen Fehler zurückgegeben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Wert der [**cbasewindow:: m \_ bnorealize**](cbasewindow-m-bnorealize.md) -Element Variablen **false** (Standardeinstellung) ist, wählt diese Methode die Palette aus und erkennt Sie. Andernfalls wird die Palette ausgewählt, aber nicht erkannt. Das Objekt löscht keine zuvor verwendete Palette. Der Aufrufer ist für das Löschen von Paletten verantwortlich.

Jeder Thread kann diese Methode sicher aufzurufen, nicht nur den Thread, der das Fenster besitzt. Das Fenster sendet eine private Nachricht an sich selbst, wodurch ein Aufrufvorgang der [**cbasewindow:: onpalettechange**](cbasewindow-onpalettechange.md) -Methode ausgelöst wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




