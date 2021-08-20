---
title: Var-Struktur
description: Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält in der Regel eine Liste der Sprachen- und Codepage-Bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Var structure Menus and Other Resources
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48537009b56d2b37f4508871049463a65a12965c31658e932716832955503f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599580"
---
# <a name="var-structure"></a>Var-Struktur

Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält in der Regel eine Liste der Sprachen- und Codepage-Bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a>Member

<dl> <dt>

**wLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Länge der **Var-Struktur** in Bytes.

</dd> <dt>

**wValueLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Länge des **Value-Members** in Bytes.

</dd> <dt>

**wType**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Datentyp in der Versionsressource. Dieser Member ist 1, wenn die Versionsressource Textdaten enthält, und 0, wenn die Versionsressource Binärdaten enthält.

</dd> <dt>

**szKey**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Die Unicode-Zeichenfolge L"Translation".

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

So viele 0 Wörter wie nötig, um das **Value-Element** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein Array von einem oder mehreren Werten, bei denen es sich um Sprach- und Codepagebezeichnerpaare handelt. Weitere Informationen finden Sie im abschnitt "Hinweise".

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist keine echte C-Sprachstruktur, da sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versionsressource erstellt und wird in keiner der Headerdateien angezeigt, die mit dem Windows Software Development Kit (SDK) ausgeliefert werden.

Wenn Sie die **Var-Struktur** verwenden, um die sprachen aufzulisten, die Ihre Anwendung oder DLL unterstützt, anstatt mehrere Versionsressourcen zu verwenden, verwenden Sie den **Value-Member,** um ein Array von **DWORD-Werten** zu enthalten, das die von dieser Datei unterstützten Sprach- und Codepagekombinationen angibt. Das Wort in niedriger Reihenfolge jedes **DWORD** muss einen Microsoft-Sprachbezeichner enthalten, und das Wort in hoher Reihenfolge muss die IBM-Codepagenummer enthalten. Ein Wort mit hoher oder niedriger Reihenfolge kann 0 (null) sein, was darauf hinweist, dass die Datei sprach- oder codepageunabhängig ist. Wenn die **Var-Struktur** ausgelassen wird, wird die Datei sowohl als sprach- als auch als codepageunabhängig interpretiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





