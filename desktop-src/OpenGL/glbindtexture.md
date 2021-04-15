---
title: glBindTexture-Funktion (GL. h)
description: Die glBindTexture-Funktion ermöglicht das Erstellen einer benannten Textur, die an ein Textur Ziel gebunden ist.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391997"
---
# <a name="glbindtexture-function"></a>glBindTexture-Funktion

Die **glBindTexture** -Funktion ermöglicht das Erstellen einer benannten Textur, die an ein Textur Ziel gebunden ist.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Das Ziel, an das die Textur gebunden ist. Muss den Wert "GL \_ Texture \_ 1D" oder "GL \_ Texture \_ 2D" aufweisen.

</dd> <dt>

*Konsistenz* 
</dt> <dd>

Der Name einer Textur. der Textur Name darf derzeit nicht verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das Parameter *Ziel* war kein akzeptierter Wert.<br/>                                                                                                                                                       |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Parameter *Textur* enthielt nicht die gleiche Dimensionalität wie das *Ziel*, oder die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Mit der **glBindTexture** -Funktion können Sie eine benannte Textur erstellen. Der Aufruf von **glBindTexture** , bei dem das *Ziel* auf GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D festgelegt ist, und die *Textur* werden auf den Namen der neuen Textur festgelegt, die Sie erstellt haben, binden den Textur Namen an das entsprechende Textur Ziel. Wenn eine Textur an ein Ziel gebunden ist, ist die vorherige Bindung für dieses Ziel nicht mehr wirksam.

Textur Namen sind ganze Zahlen ohne Vorzeichen, wobei der Wert 0 (null) für die Darstellung der Standard Textur für die einzelnen Textur Ziele reserviert ist. Textur Namen und die entsprechenden Textur Inhalte sind lokal im freigegebenen Anzeigelisten Bereich des aktuellen OpenGL-renderingkontexts. zwei renderingkontexte geben Textur Namen nur dann frei, wenn Sie auch anzeigen Listen freigeben. Sie können mit [**glgentexturen**](glgentextures.md)eine Reihe neuer Textur Namen generieren.

Wenn eine Textur zum ersten Mal gebunden wird, wird davon ausgegangen, dass die Dimensionalität des zugehörigen Textur Ziels liegt. eine Textur, die an GL \_ Texture \_ 1D gebunden ist, wird eindimensional, und eine Textur, die an GL \_ Texture 2D gebunden ist, \_ wird zweidimensional. Vorgänge, die Sie für ein Textur Ziel ausführen, wirken sich auch auf eine Textur aus, die an das Ziel gebunden Wenn Sie ein Textur Ziel Abfragen, ist der Rückgabewert der Zustand der an ihn gebundenen Textur. Textur Ziele werden Aliase für Texturen, die zurzeit an Sie gebunden sind.

Wenn Sie eine Textur mit **glBindTexture** binden, bleibt die Bindung aktiv, bis eine andere Textur an dasselbe Ziel gebunden ist oder Sie die gebundene Textur mit der Funktion " [**gldeletetexturen**](gldeletetextures.md) " löschen. Nachdem Sie eine benannte Textur erstellt haben, können Sie Sie an ein Textur Ziel binden, das über dieselbe Dimensionalität verfügt wie bei Bedarf.

Es ist in der Regel viel schneller, eine vorhandene benannte Textur mithilfe von **glBindTexture** an eines der Textur Ziele zu binden, als das Textur Bild mithilfe von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md)neu zu laden. Verwenden Sie zum zusätzlichen Steuern der texturierungs Leistung [**glpriorizetexturen**](glprioritizetextures.md).

Sie können Aufrufe von **glBindTexture** in Anzeigelisten einschließen.

> [!Note]  
> Die **glBindTexture** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glBindTexture** abgerufen:

-   [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Texture \_ 1D \_ Binding

**glget** mit Argument GL \_ Texture \_ 2D \_ Binding

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

[**gldeletetexturen**](gldeletetextures.md)
</dt> <dt>

[**glgentexturen**](glgentextures.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glistexture**](glistexture.md)
</dt> <dt>

[**glpriorizetexturen**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gltexparameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





