---
title: glShadeModel-Funktion (Gl.h)
description: Die glShadeModel-Funktion wählt flache oder flache Schattierung aus.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel-Funktion OpenGL
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
ms.openlocfilehash: 505ff0e2d74f9eb4f252e4e663ceec00fd86469b3d69374623b2763915a08b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491610"
---
# <a name="glshademodel-function"></a>glShadeModel-Funktion

Die **glShadeModel-Funktion** wählt flache oder flache Schattierung aus.

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

Ein symbolischer Wert, der eine Schattierungstechnik darstellt. Akzeptierte Werte sind GL \_ FLAT und GL \_ SMOOTH. Der Standardwert ist GL \_ SMOOTH.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war ein anderer Wert als GL \_ SMOOTHT oder \_ GL SMOOTH.<br/>                                                                      |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

OpenGL-Primitive können entweder flache oder flache Schattierung haben. Die schattierte Schattierung (Standardeinstellung) bewirkt, dass die berechneten Farben von Scheitelpunkts interpoliert werden, während das Primitiv rastert, wodurch jedem resultierenden Pixelfragment in der Regel unterschiedliche Farben zugewiesen werden. Flache Schattierung wählt die berechnete Farbe nur eines Scheitelpunkts aus und weist sie allen Pixelfragmenten zu, die durch Rastern eines einzelnen Primitiven generiert werden. In beiden Fällen ist die berechnete Farbe eines Scheitelpunkts das Ergebnis der Beleuchtung, wenn die Beleuchtung aktiviert ist, oder die aktuelle Farbe zum Zeitpunkt der Angabe des Scheitelpunkts, wenn die Beleuchtung deaktiviert ist.

Flache und gleichmäßige Schattierung sind für Punkte nicht zu unterscheiden. Beim Zählen von Scheitelpunkte und Primitiven von 1 erhält jedes flach schattierte Liniensegment *i* ab der Zählung von [**glBegin**](glbegin.md) die berechnete Farbe des Scheitelpunkts *i* + 1, seines zweiten Scheitelpunkts. Auf ähnliche Weise wird jedem flach schattierten Polygon die berechnete Farbe des scheitelpunkts in der folgenden Tabelle gegeben. Dies ist der letzte Scheitelpunkt, der das Polygon in allen Fällen mit Ausnahme einzelner Polygone angibt, wobei der erste Scheitelpunkt die flach schattierte Farbe angibt.



| Primitiver Polygontyp i | Scheitelpunkt   |
|-----------------------------|----------|
| Einzelnes Polygon (*I*=1)      | 1        |
| Dreiecksstreifen              | *i* + 2  |
| Dreiecksfächer                | *i* + 2  |
| Unabhängiges Dreieck        | 3 *I*     |
| Quad-Strip                  | 2 *i* + 2 |
| Unabhängiges Quad            | 4 *I*     |



 

Flache und gleichmäßige Schattierung werden von **glShadeModel** angegeben, und *der Modus* ist auf GL FLAT bzw. GL \_ SMOOTH \_ festgelegt.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glShadeModel ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ SHADE \_ MODEL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





