---
description: Die FORM_INFO_1-Struktur enthält Informationen zu einem Druckformular. Die Informationen umfassen den Ursprung der Druckformulare, ihren Namen, ihre Dimensionen und die Abmessungen des druckbaren Bereichs.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: FORM_INFO_1 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6f620d8bd2ed4ef39fc868c91068e10a7ff43f57d98510ecfbae1dbe2ae7c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949260"
---
# <a name="form_info_1-structure"></a>FORM_INFO_1-Struktur

Die **FORM_INFO_1-Struktur** enthält Informationen zu einem Druckformular. Die Informationen umfassen den Ursprung des Druckformulars, seinen Namen, seine Dimensionen und die Abmessungen des druckbaren Bereichs.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Die Formulareigenschaften. Die folgenden Werte werden definiert.



| Wert         | Bedeutung                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | Wenn dieses Bitflag festgelegt ist, wurde das Formular vom Benutzer definiert. Formulare, für die dieses Flag festgelegt ist, werden in der Registrierung definiert.        |
| FORM_BUILTIN | Wenn dieses Bitflag festgelegt ist, ist das Formular Teil des Spoolers. Formulardefinitionen, für die dieses Flag festgelegt ist, werden nicht in der Registrierung angezeigt. |
| FORM_PRINTER | Wenn dieses Bitflag festgelegt ist, wird das Formular einem bestimmten Drucker zugeordnet, und seine Definition wird in der Registrierung angezeigt.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Formulars angibt. Der Formularname darf 31 Zeichen nicht überschreiten.

</dd> <dt>

**Größe**
</dt> <dd>

Die Breite und Höhe des Formulars in Tausendstel Millimeter.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Die Breite und Höhe des Formulars in Tausendstel Millimeter.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **_FORM_INFO_1W** (Unicode) und **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




