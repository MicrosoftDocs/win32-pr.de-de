---
description: Die Methode initialierwindow initialisiert das Fenster.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Initialierwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371108"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.Initialierwindow-Methode

Die- `InitialiseWindow` Methode initialisiert das-Fenster.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle für das Fenster.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Standardmäßig ruft diese Methode ein Handle für den Gerätekontext des Fensters ab und erstellt einen kompatiblen Arbeitsspeicher-DC. Wenn der Wert des [**cbasewindow:: m \_ bdogetdc**](cbasewindow-m-bdogetdc.md) -Flags **false** ist, ruft diese Methode jedoch nicht die Geräte Kontexte ab. Der Arbeitsspeicher-Domänen Controller eignet sich für die Auswahl von Bitmaps, bevor diese im Fenster ausgeblendet werden.

Die [**cbasewindow::D okreatewindow**](cbasewindow-docreatewindow.md) -Methode ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




