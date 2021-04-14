---
title: gldrawelements-Funktion (GL. h)
description: Die gldrawelements-Funktion rendert primitive aus Array Daten.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- gldrawelements-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518101"
---
# <a name="gldrawelements-function"></a>gldrawelements-Funktion

Die **gldrawelements** -Funktion rendert primitive aus Array Daten.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die Art der zu Rendering enden primitiver. Es kann von einem der folgenden symbolischen Werte ausgegangen werden: GL- \_ Punkte, GL-Linien \_ \_ Streifen, GL \_ -Zeilen \_ Schleife, GL \_ -Linien, GL \_ \_ -Dreiecks Streifen, GL \_ \_ -Dreiecks Lüfter, GL \_ -Dreiecke, GL \_ Quad Strip, \_ GL \_ QUADS und GL- \_ Polygon.

</dd> <dt>

*count* 
</dt> <dd>

Die Anzahl der Elemente, die gerendert werden sollen.

</dd> <dt>

*type* 
</dt> <dd>

Der Typ der Werte in Indizes. Es muss sich um ein "GL \_ unsigned \_ Byte", "GL \_ unsigned \_ Short" oder "GL \_ unsigned \_ int" handeln.

</dd> <dt>

*Kei* 
</dt> <dd>

Ein Zeiger auf den Speicherort, an dem die Indizes gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *count* war ein negativer Wert.<br/>                                                                                              |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Mit der **gldrawelements** -Funktion können Sie mehrere geometrische Primitive mit sehr wenigen Funktionsaufrufen angeben. Anstatt eine OpenGL-Funktion aufzurufen, um die einzelnen Scheitel Punkte, normal oder Farben zu übergeben, können Sie im Vorfeld separate Arrays von Scheitel Punkten, normalen und Farben angeben und diese zum Definieren einer Sequenz von primitiven (alle desselben Typs) mit einem einzigen Aufruf von **gldrawelements** verwenden.

Wenn Sie die **gldrawelements** -Funktion aufzurufen, *werden sequenzielle* Elemente aus *Indizes* verwendet, um eine Sequenz geometrischer primitiver Elemente zu erstellen. Der *Mode* -Parameter gibt an, welche Art von primitiver Typen erstellt werden und wie die Array Elemente verwendet werden, um diese primitiven zu konstruieren. Wenn das GL- \_ Scheitelpunkt \_ Array nicht aktiviert ist, werden keine geometrischen primitiven generiert.

Vertex-Attribute, die von **gldrawelements** geändert werden, haben nach dem zurückkehren von **gldrawelements** einen nicht angegebenen Wert. Wenn z. b. \_ das GL- \_ Farbarray aktiviert ist, ist der Wert der aktuellen Farbe nach der Ausführung von **gldrawelements** nicht definiert. Attribute, die nicht geändert werden, bleiben unverändert.

Sie können die **gldrawelements** -Funktion in Anzeigelisten einschließen. Wenn **gldrawelements** in einer Anzeigeliste enthalten ist, werden die erforderlichen Array Daten (festgelegt durch die Array Zeiger und die Aktivierung) ebenfalls in die Anzeigeliste eingegeben. Da die Array Zeiger und-Aktivierung Client seitige Zustandsvariablen sind, beeinflussen Ihre Werte die Anzeigelisten, wenn die Listen erstellt werden, und nicht, wenn die Listen ausgeführt werden.

> [!Note]  
> Die **gldrawelements** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

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

[**glarrayelement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolorpointer**](glcolorpointer.md)
</dt> <dt>

[**gldrawarrays**](gldrawarrays.md)
</dt> <dt>

[**gledgeflagpointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgetpointerv**](glgetpointerv.md)
</dt> <dt>

[**glindexpointer**](glindexpointer.md)
</dt> <dt>

[**glnormalpointer**](glnormalpointer.md)
</dt> <dt>

[**gltexcoordpointer**](gltexcoordpointer.md)
</dt> <dt>

[**glvertexpointer**](glvertexpointer.md)
</dt> </dl>

 

 





