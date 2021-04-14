---
title: glpolygonoffset-Funktion (GL. h)
description: Die Funktion "glpolygonoffset" legt die Skala und Einheiten fest, die OpenGL zum Berechnen von tiefen Werten verwendet.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glpolygonoffset-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391989"
---
# <a name="glpolygonoffset-function"></a>glpolygonoffset-Funktion

Die Funktion " **glpolygonoffset** " legt die Skala und Einheiten fest, die OpenGL zum Berechnen von tiefen Werten verwendet.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*gebend* 
</dt> <dd>

Gibt einen Skalierungsfaktor an, der zum Erstellen eines Variablen tiefen Offsets für jedes Polygon verwendet wird. Der Anfangswert ist 0 (null).

</dd> <dt>

*Einrichtungen* 
</dt> <dd>

Gibt einen Wert an, der mit einem Implementierungs spezifischen Wert multipliziert wird, um einen konstanten tiefen Offset zu erstellen. Der Anfangswert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn \_ der GL \_ -Polygon Offset aktiviert ist, wird der tiefen Wert jedes Fragments versetzt, nachdem er von den tiefen Werten der entsprechenden Scheitel Punkte interpoliert wurde. Der Wert des Offsets ist *Factor* \* ? z + r- \* *Einheiten*, wobei? z eine Maßeinheit für die Tiefe der Änderung relativ zum Bildschirmbereich des Polygons ist, und r ist der kleinste Wert, der garantiert einen auflösbaren Offset für eine bestimmte Implementierung erzeugt. Der Offset wird hinzugefügt, bevor der tiefen Test durchgeführt wird und bevor der Wert in den tiefen Puffer geschrieben wird.

Die Funktion " **glpolygonoffset** " eignet sich zum Rendern von ausgeblendeten Bildern, zum Anwenden von decds auf Oberflächen und zum Rendern von Festplatten mit hervorgehobenen Kanten.

Die Funktion " **glpolygonoffset** " hat keine Auswirkung auf die tiefen Koordinaten, die im Feedback Puffer abgelegt werden. Außerdem hat es keine Auswirkung auf die Auswahl.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpolygonoffset** ab:

-   [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Polygon- \_ Offset \_ Faktor
-   [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Polygon- \_ Offset \_ Einheiten
-   [**glisenabled**](glisenabled.md) mit Argument GL \_ Polygon \_ Offset \_ Fill
-   [**glisenabled**](glisenabled.md) mit Argument GL \_ Polygon- \_ Versatz \_ Linie
-   [**glisenabled**](glisenabled.md) mit dem Argument GL \_ Polygon \_ Offset \_ Point

> [!Note]  
> Die Funktion " **glpolygonoffset** " ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

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

[**gldepthfunc**](gldepthfunc.md)
</dt> <dt>

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glstencilop**](glstencilop.md)
</dt> <dt>

[**gltexd**](gltexenv-functions.md)
</dt> </dl>

 

 





