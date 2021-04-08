---
title: glpriorizetexturen-Funktion (GL. h)
description: Die Funktion "glpriorizetexturen" legt die Residenz Priorität von Texturen fest.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glpriorizetexturen-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740648"
---
# <a name="glprioritizetextures-function"></a>glpriorizetexturen-Funktion

Die Funktion " **glpriorizetexturen** " legt die Residenz Priorität von Texturen fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Anzahl der Texturen, die priorisiert werden sollen.

</dd> <dt>

*Textur* 
</dt> <dd>

Ein Zeiger auf das erste Element eines Arrays mit den Namen der Texturen, die priorisiert werden sollen.

</dd> <dt>

*Prioritäten* 
</dt> <dd>

Ein Zeiger auf das erste Element eines Arrays, das die Textur Prioritäten enthält. Eine Priorität, die in einem Element des *Prioritäten* -Parameters angegeben wird, gilt für die Textur, die durch das entsprechende Element des *Texturen* -Parameters benannt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *n* war ein negativer Wert.<br/>                                                                                                  |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glpriorizetexturen** " weist die im Parameter " *Prioritäten* " *angegebenen n-Textur Prioritäten* den *n* -Texturen zu, die im *Texturen* -Parameter genannt werden. Auf Computern mit einer begrenzten Menge an Textur Arbeitsspeicher erstellt OpenGL einen "Workingset" von Texturen, die im Texturspeicher ansässig sind. Diese Texturen können wesentlich effizienter an ein Textur Ziel gebunden werden als nicht residente Texturen.

Durch die Angabe einer Priorität für jede Textur können Sie mit der Funktion " **glpriorizetexturen** " bestimmen, welche Texturen ansässig sein sollten.

Die Elemente der Textur Prioritäten *werden an* den Bereich \[ 0,0 und 1,0 gebunden, \] bevor Sie zugewiesen werden. NULL gibt die niedrigste Priorität an. Daher ist die Wahrscheinlichkeit, dass Texturen mit der Priorität 0 (null) wahrscheinlich nicht in der Der Wert 1,0 gibt die höchste Priorität an. Folglich sind Texturen mit Priorität 1,0 höchstwahrscheinlich ansässig. Es ist jedoch nicht gewährleistet, dass Texturen in den residenten Leben, bis Sie gebunden sind.

Die Funktion " **glpriorizetexturen** " ignoriert Versuche, Textur 0 oder einen beliebigen Textur Namen zu priorisieren, der keiner vorhandenen Textur entspricht. Keine der Funktionen, die durch den *Texturen* -Parameter benannt werden, muss an ein Textur Ziel gebunden werden.

Wenn eine Textur momentan gebunden ist, können Sie auch die [**gltexparameter**](gltexparameter-functions.md) -Funktion verwenden, um die Priorität festzulegen. Dies ist die einzige Möglichkeit, die Priorität einer Standard Textur festzulegen.

Sie können **glpriorizetexturen** in Anzeigelisten einschließen.

Die folgende Funktion Ruft die Priorität einer zurzeit gebundenen Textur ab, die sich auf **glpriorizetexturen** bezieht:

-   [**glgettexparameter**](glgettexparameter.md) mit Parameter Name GL \_ Textur \_ Priorität

> [!Note]  
> Die Funktion " **glpriorizetexturen** " ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

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

[**glaretexturesresidente**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





