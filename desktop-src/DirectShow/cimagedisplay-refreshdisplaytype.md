---
description: Die RefreshDisplayType-Methode aktualisiert das Videoformat des Objekts so, dass es mit der angegebenen Anzeige übereinstimmen kann.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: CImageDisplay.RefreshDisplayType-Methode (Winutil.h)
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
ms.openlocfilehash: d9184d5e8a0e0ad6c0242ec1dc4b7590f1bc0d39a0a9cd6a09b2676563a2796e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055470"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>CImageDisplay.RefreshDisplayType-Methode

Die `RefreshDisplayType` -Methode aktualisiert das Videoformat des Objekts so, dass es mit der angegebenen Anzeige übereinstimmen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szDeviceName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeigegeräts enthält, wie von der **GDI-Funktion EnumDisplayDevices** zurückgegeben. Um das Hauptanzeigegerät zu verwenden, legen Sie diesen Parameter auf **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder E \_ FAIL, wenn nicht erfolgreich.

## <a name="remarks"></a>Hinweise

Diese Methode initialisiert den **m \_ Display-Member** mit einem Videotyp, der dem Anzeigemodus auf dem angegebenen Gerät entspricht.

Rufen Sie diese Methode auf, wenn eine WM \_ DISPLAYCHANGED-Nachricht empfangen wird, oder , um ein sekundäres Anzeigegerät anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




