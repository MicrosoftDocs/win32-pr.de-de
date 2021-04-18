---
title: glshademodel-Funktion (GL. h)
description: Die glshademodel-Funktion wählt Flat-oder Smooth-Schattierung aus.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glshademodel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339958"
---
# <a name="glshademodel-function"></a>glshademodel-Funktion

Die **glshademodel** -Funktion wählt Flat-oder Smooth-Schattierung aus.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Ein symbolischer Wert, der eine Schattierungs Technik darstellt. Akzeptierte Werte sind GL \_ Flat und GL \_ Smooth. Der Standardwert ist "GL \_ Smooth".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war ein anderer Wert als GL \_ glat oder GL \_ Smooth.<br/>                                                                      |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

OpenGL-primitive können entweder flach oder Smooth Schattierung aufweisen. Die standardmäßige Schattierung bewirkt, dass die berechneten Farben der Scheitel Punkte interpoliert werden, wenn der primitive gerendert wird. in der Regel werden jedem resultierenden Pixel Fragment verschiedene Farben zugewiesen. Die flache Schattierung wählt die berechnete Farbe nur eines Scheitel Punkts aus und weist diese allen Pixel Fragmenten zu, die durch das rasterieren eines einzelnen primitiven generiert werden. In beiden Fällen ist die berechnete Farbe eines Scheitel Punkts das Ergebnis der Beleuchtung, wenn Beleuchtung aktiviert ist, oder es handelt sich um die aktuelle Farbe zum Zeitpunkt der Angabe des Scheitel Punkts, wenn die Beleuchtung deaktiviert ist.

Flache und glatte Schattierung können nicht für Punkte unterschieden werden. Beim zählen von Scheitel Punkten und primitiven von einem, beginnend bei der Ausgabe von [**glBegin**](glbegin.md) , erhält jedes flach schattierte *Liniensegment die* berechnete Farbe des Scheitel Punkts *i* + 1, dessen zweiter Scheitelpunkt. Wenn Sie auf ähnliche Weise gezählt werden, erhält jedes flatschattierte Polygon die berechnete Farbe des Vertex, der in der folgenden Tabelle aufgeführt ist. Dies ist der letzte Scheitelpunkt zum Angeben des Polygons in allen Fällen außer einzelnen Polygonen, wobei der erste Scheitelpunkt die flache schattierte Farbe angibt.



| Primitiver Typ von Polygon i | Scheitelpunkt   |
|-----------------------------|----------|
| Einzelnes Polygon (*I*= 1)      | 1        |
| Dreiecks Streifen              | *i* + 2  |
| Dreiecks Lüfter                | *i* + 2  |
| Unabhängiges Dreieck        | 3 *I*     |
| Quad-Strip                  | 2 *i* + 2 |
| Unabhängiges Quad            | 4 *I*     |



 

Die flache und die glatte Schattierung werden von **glshademodel** angegeben, wobei der *Modus* auf GL \_ Flat \_ bzw. gl Smooth festgelegt ist.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glshademodel** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Schattierung- \_ Modell

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

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**gllight**](gllight-functions.md)
</dt> <dt>

[**gllightmodel**](gllightmodel-functions.md)
</dt> </dl>

 

 





