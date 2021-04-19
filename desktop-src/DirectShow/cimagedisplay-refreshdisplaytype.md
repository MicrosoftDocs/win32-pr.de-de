---
description: Die Methode "Aktualisierungs Methode" aktualisiert das Videoformat des Objekts entsprechend der angegebenen Anzeige.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Cimagedisplay. erfrischend Display Type-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366744"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>Cimagedisplay. erfrischend Display Type-Methode

Die `RefreshDisplayType` -Methode aktualisiert das Videoformat des Objekts entsprechend der angegebenen Anzeige.

## <a name="syntax"></a>Syntax


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szdevicename* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben. Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück, oder E \_ schlägt fehl, wenn er nicht erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Methode initialisiert den **m- \_ Anzeige** Member mit einem Videotyp, der dem Anzeigemodus auf dem angegebenen Gerät entspricht.

Ruft diese Methode immer dann auf, wenn eine "WM \_ Display Changed"-Meldung empfangen wird, oder um ein sekundäres Anzeigegerät anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




