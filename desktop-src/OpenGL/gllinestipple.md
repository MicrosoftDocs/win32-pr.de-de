---
title: gllinestippel-Funktion (GL. h)
description: Die gllinestippel-Funktion gibt das Zeilen stippingmuster an.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- gllinestippel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739800"
---
# <a name="gllinestipple-function"></a>gllinestippel-Funktion

Die **gllinestippel** -Funktion gibt das Zeilen stippingmuster an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*gebend* 
</dt> <dd>

Ein Multiplikator für jedes Bit im Zeilen stippingmuster. Wenn der *Faktor* z. b. 3 ist, wird jedes Bit im Muster dreimal verwendet, bevor das nächste Bit im Muster verwendet wird. Der *Faktor* Parameter wird an den Bereich \[ 1, 256 und der \] Standardwert auf einen Wert gebunden.

</dd> <dt>

*pattern* 
</dt> <dd>

Eine 16-Bit-Ganzzahl, deren Bitmuster bestimmt, welche Fragmente einer Linie gezeichnet werden, wenn die Linie gerengt wird. Zuerst wird Bit 0 verwendet, und das Standardmuster ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **gllinestippel** -Funktion gibt das Zeilen stippingmuster an. Zeilen stippling maskiert bestimmte Fragmente, die von der rasterization erzeugt werden. Diese Fragmente werden nicht gezeichnet. Die Maskierung wird durch die Verwendung von drei Parametern erreicht: das Muster *Muster* für 16-Bit-Zeilen Stippel, der Wiederholungs Zähler *Faktor* und ein ganzzahliger stippingzähler *.*

Der Wert für " *s* " wird auf 0 (null) zurückgesetzt, wenn " [**glBegin**](glbegin.md) " aufgerufen wird und bevor jedes Liniensegment einer **glBegin**(GL \_ Lines)/**glEnd** -Sequenz generiert wird. Sie wird inkrementiert, nachdem jedes Fragment eines Einheiten Bereichs mit einem einzelnen Zeilen Segment generiert wurde, oder nachdem die einzelnen *i* -Fragmente eines *i* -breiten Linien Segments generiert wurden. Die der Anzahl *s* zugeordneten *i* -Fragmente werden maskiert, wenn der *Pattern* -Bit (*s*-  /  *Faktor*) mod 16 0 (null) ist. Andernfalls werden diese Fragmente an den Framebuffer-Puffer gesendet. Bit 0 (null) des *Musters* ist das am wenigsten bedeutende Bit.

Antialiasing-Zeilen werden als Sequenz von 1X-*breiten* Rechtecke für stippling behandelt. Die *Rechtecke* sind rasterisiert oder nicht basierend auf der fragmentregel, die für Alias Zeilen beschrieben wird. Sie zählt anstelle von Gruppen von Fragmenten Rechtecke.

Das Zeilen stippling ist mit " [**glEnable**](glenable.md) " und " **glEnable** " mit dem Argument "GL \_ Line Stippel" aktiviert oder deaktiviert \_ . Wenn diese Option aktiviert ist, wird das Zeilen stippingmuster wie oben beschrieben angewendet. Wenn diese Option deaktiviert ist, ist es so, als ob es sich um das Muster handelt. Anfänglich ist das Zeilen stippling deaktiviert.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gllinestippel** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Zeilen \_ stippingmuster \_

**glget** mit dem Argument GL \_ Zeilen \_ Stippel \_ Wiederholen

[**glisenabled**](glisenabled.md) mit Argument GL- \_ Zeilen \_ Stippel

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

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glpolygonstippel**](glpolygonstipple.md)
</dt> </dl>

 

 





