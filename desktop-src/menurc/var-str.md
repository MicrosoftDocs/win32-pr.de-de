---
title: Var-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält in der Regel eine Liste der Sprachen-und Codepage-bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Var Structure-Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859257"
---
# <a name="var-structure"></a>Var-Struktur

Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält in der Regel eine Liste der Sprachen-und Codepage-bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.

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

**wlength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge der **var** -Struktur in Bytes.

</dd> <dt>

**wvaluelength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge (in Byte) des **Wertmembers** .

</dd> <dt>

**wType**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Typ der Daten in der Versions Ressource. Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.

</dd> <dt>

**szkey**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Die Unicode-Zeichenfolge L "Translation".

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **Word**

</dd> <dd>

So viele Null-Wörter, wie erforderlich, um den **Wertmember** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein Array von einem oder mehreren Werten, die Sprach-und Codepage-bezeichnerpaare sind. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.

Wenn Sie die **var** -Struktur verwenden, um die Sprachen aufzulisten, die Ihre Anwendung oder DLL unterstützt, anstatt mehrere Versions Ressourcen zu verwenden, verwenden Sie das **Wertmember** , um ein Array von **DWORD** -Werten anzugeben, die die von dieser Datei unterstützten Kombinationen von Sprache und Codepage angeben Das nieder wertige Wort jedes **DWORD** muss einen Microsoft-Sprachen Bezeichner enthalten, und das höchst wertige Wort muss die IBM-Code Page Nummer enthalten. Ein Wort mit hoher Reihenfolge oder niedriger Ordnung kann NULL sein, was darauf hinweist, dass die Datei sprach-oder Codepage-unabhängig ist. Wenn die **var** -Struktur weggelassen wird, wird die Datei als Sprache und Codepage unabhängig interpretiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Varfileingefo**](varfileinfo.md)
</dt> <dt>

[**Stringfileingefo**](stringfileinfo.md)
</dt> <dt>

[**STRINGTABLE**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





