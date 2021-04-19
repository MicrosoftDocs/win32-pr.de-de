---
description: Die FORM_INFO_1-Struktur enthält Informationen zu einem Druckformular. Die Informationen umfassen den Ursprung der Druckformulare, den Namen, die Dimensionen und die Dimensionen des druckbaren Bereichs.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: FORM_INFO_1 Struktur (winspool. h)
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
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373125"
---
# <a name="form_info_1-structure"></a>FORM_INFO_1 Struktur

Die **FORM_INFO_1** -Struktur enthält Informationen zu einem Druckformular. Die Informationen umfassen den Ursprung des Druck Formulars, den Namen, seine Dimensionen und die Abmessungen des druckbaren Bereichs.

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

Die Formular Eigenschaften. Die folgenden Werte sind definiert.



| Wert         | Bedeutung                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | Wenn dieses Bitflag festgelegt ist, wurde das Formular vom Benutzer definiert. Formulare mit diesem Flagsatz werden in der Registrierung definiert.        |
| FORM_BUILTIN | Wenn dieses Bitflag festgelegt ist, ist das Formular Teil des Spoolers. Formular Definitionen mit diesem Flagsatz werden nicht in der Registrierung angezeigt. |
| FORM_PRINTER | Wenn dieses Bitflag festgelegt ist, wird das Formular einem bestimmten Drucker zugeordnet, und seine Definition wird in der Registrierung angezeigt.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Formulars angibt. Der Formular Name darf nicht länger als 31 Zeichen sein.

</dd> <dt>

**Größe**
</dt> <dd>

Die Breite und Höhe des Formulars in tausendstel Millimeter.

</dd> <dt>

**Imageablearea**
</dt> <dd>

Die Breite und Höhe des Formulars in tausendstel Millimeter.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **_FORM_INFO_1W** (Unicode) und **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**Setform**](setform.md)
</dt> </dl>

 

 




