---
title: glgetpolygonstippel-Funktion (GL. h)
description: Die glgetpolygonstippel-Funktion gibt das Polygon Stippel Muster zurück.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glgetpolygonstippel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858724"
---
# <a name="glgetpolygonstipple-function"></a>glgetpolygonstippel-Funktion

Die **glgetpolygonstippel** -Funktion gibt das Polygon Stippel Muster zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Gibt das Stippel Muster zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glgetpolygonstippel** -Funktion gibt ein Polygon stippingmuster mit einem 32x32-Polygon durch den *Mask* -Parameter zurück. Das Muster wird in den Arbeitsspeicher verpackt, als ob [**glread Pixels**](glreadpixels.md) sowohl mit der *Höhe* als auch mit der *Breite* 32, dem *Typ* der GL \_ -Bitmap und dem *Format* des GL \_ \_ -Farbindexes aufgerufen und das stippingmuster in einem internen 32 x 32-Farb Index Puffer gespeichert wurde. Im Gegensatz zu **gllepixels** werden Pixel Übertragungs Vorgänge (Shift, Offset und Pixel Map) jedoch nicht auf das zurückgegebene Stippel Bild angewendet.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Maske* vorgenommen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glpolygonstippel**](glpolygonstipple.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> </dl>

 

 





