---
title: glIndexf-Funktion (Gl.h)
description: Die glIndexf-Funktion legt den aktuellen Farbindex fest.
ms.assetid: 1109c6b0-daf6-4b93-8e9e-5dd542b6f7c8
keywords:
- glIndexf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb53fa34ff3723fc8539f547627b985ea2884b0dffd7d83a431e26acb25a2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359528"
---
# <a name="glindexf-function"></a>glIndexf-Funktion

Die **glIndexf-Funktion** legt den aktuellen Farbindex fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glIndexf(
   GLfloat c
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*c* 
</dt> <dd>

Der neue Wert für den aktuellen Farbindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glIndexf-Funktion** aktualisiert den aktuellen (einwertigen) Farbindex. Es wird ein Argument verwendet: der neue Wert für den aktuellen Farbindex.

Der aktuelle Index wird als Gleitkommawert gespeichert. Ganzzahlige Werte werden ohne spezielle Zuordnung direkt in Gleitkommawerte konvertiert.

Indexwerte außerhalb des darstellbaren Bereichs des Farbindexpuffers werden nicht geklammert. Bevor ein Index jedoch gedithert (sofern aktiviert) und in den Framepuffer geschrieben wird, wird er in das Festpunktformat konvertiert. Alle Bits im ganzzahligen Teil des resultierenden Festpunktwerts, die bits im Framepuffer nicht entsprechen, werden maskiert.

Der aktuelle Index kann jederzeit aktualisiert werden. Insbesondere kann **glIndexf** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd aufgerufen werden.**](glend.md)

Die folgende Funktion ruft Informationen im Zusammenhang mit **glIndexf ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ CURRENT \_ INDEX

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

