---
title: glstencilmask-Funktion (GL. h)
description: Die Funktion "glstencilmask" steuert das Schreiben einzelner Bits in den Schablonen Ebenen.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glstencilmask-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106400"
---
# <a name="glstencilmask-function"></a>glstencilmask-Funktion

Die Funktion " **glstencilmask** " steuert das Schreiben einzelner Bits in den Schablonen Ebenen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Eine Bitmaske zum Aktivieren und Deaktivieren der Erstellung einzelner Bits in den Schablonen Ebenen. Anfänglich ist die Maske alle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glstencilmask** " steuert das Schreiben einzelner Bits in den Schablonen Ebenen. Die am wenigsten signifikanten *n* Bits der *Maske*, wobei *n* die Anzahl der Bits im Schablonen Puffer ist, geben eine Maske an. Wenn eine in der Maske angezeigt wird, wird das entsprechende Bit im Schablonen Puffer beschreibbar gemacht. Wenn ein NULL-Wert angezeigt wird, ist das Bit schreibgeschützt. Anfänglich werden alle Bits zum Schreiben aktiviert.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit " **glstencilmask**" ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ schreibfrage

glget mit Argument GL- \_ Schablonen \_ Bits

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

[**glcolormask**](glcolormask.md)
</dt> <dt>

[**gldepthmask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glindexmask**](glindexmask.md)
</dt> <dt>

[**glstencilfunc**](glstencilfunc.md)
</dt> <dt>

[**glstencilop**](glstencilop.md)
</dt> </dl>

 

 





