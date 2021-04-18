---
title: glaretexturesresidente-Funktion (GL. h)
description: Die glaretexturesresidente-Funktion bestimmt, ob angegebene Textur Objekte im Texturspeicher ansässig sind.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glaretexturesresidente-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338550"
---
# <a name="glaretexturesresident-function"></a>glaretexturesresidente-Funktion

Die **glaretexturesresidente** -Funktion bestimmt, ob angegebene Textur Objekte im Texturspeicher ansässig sind.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Anzahl der Texturen, die abgefragt werden sollen.

</dd> <dt>

*Textur* 
</dt> <dd>

Die Adresse eines Arrays mit den Namen der zu abgefragten Texturen.

</dd> <dt>

*Heimen* 
</dt> <dd>

Die Adresse eines Arrays, in dem der Status der Textur Residenz zurückgegeben wird. Der Wohnsitz Status einer Textur, die durch ein Element von *Texturen* benannt wird, wird im entsprechenden-Element von- *Residenzen* zurückgegeben.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *n* war ein negativer Wert, ein Element in *Texturen* war NULL, oder ein Element in *Texturen* enthielt keinen Textur Bezeichner.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>     |



## <a name="remarks"></a>Bemerkungen

Auf Computern mit einer begrenzten Menge an Textur Arbeitsspeicher erstellt OpenGL einen Funktions Satz von Texturen, die im Texturspeicher ansässig sind. Diese Texturen können wesentlich effizienter an ein Textur Ziel gebunden werden als nicht residente Texturen.

Die **glaretexturesresidente** -Funktion fragt den Textur Residenz Status der *n* Texturen ab, die von den Elementen der *Texturen* benannt werden. Wenn alle benannten Texturen Residenten sind, gibt **glaretexturesresidenten** den Wert "GL true" zurück \_ , und die Inhalte der residenten werden nicht beeinträchtigt.  Wenn eine der benannten Texturen nicht Resident ist, gibt **glaretexturesresidenten** den Wert "GL false" zurück \_ , und der ausführliche Status wird in den *n* -Elementen von Residenten zurückgegeben.

Wenn ein Element von *Residenzen* den Wert GL \_ true hat, ist die Textur, die durch das entsprechende Element von *Texturen* benannt ist, im Texturspeicher ansässig.

Um den Status einer einzelnen gebundenen Textur abzufragen, nennen Sie [**glgettexparameter**](glgettexparameter.md) , wobei der *Ziel* Parameter auf die Ziel Textur festgelegt ist, an die das Ziel gebunden ist, und legen Sie den Parameter " *PName* " auf "GL \_ Texture \_ residente" fest. Sie müssen diese Methode verwenden, um den residenten Status einer Standard Textur abzufragen.

Sie können **glaretexturesresidenten** nicht in Anzeigelisten einschließen.

Die **glaretexturesresidente** -Funktion gibt den Residenz Status der Texturen zum Aufruf Zeitpunkt zurück. Es wird nicht garantiert, dass die Texturen zu einem beliebigen Zeitpunkt verbleiben.

Wenn sich Texturen im virtuellen Speicher befinden (es gibt keinen Texturspeicher), werden Sie als "immer ansässig" betrachtet.

> [!Note]  
> Die **glaretexturesresidente** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glpriorizetexturen**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





