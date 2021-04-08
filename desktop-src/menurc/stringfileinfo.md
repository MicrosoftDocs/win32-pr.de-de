---
title: Stringfileingefo-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Stringfileingefo-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949551"
---
# <a name="stringfileinfo-structure"></a>Stringfileingefo-Struktur

Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>Member

<dl> <dt>

**wlength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge des gesamten **stringfileinfo** -Blocks in Bytes, einschließlich aller **vom untergeordneten** Element angegeben Strukturen.

</dd> <dt>

**wvaluelength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Dieser Member ist immer gleich 0 (null).

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

Die Unicode-Zeichenfolge L "stringfileingefo".

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **Word**

</dd> <dd>

So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **[ **STRINGTABLE**](stringtable.md)**

</dd> <dd>

Ein Array mit einem oder mehreren [**STRINGTABLE**](stringtable.md) -Strukturen. Jeder **szkey** -Member der **STRINGTABLE** -Struktur gibt die entsprechende Sprache und Codepage zum Anzeigen des Texts in der **STRINGTABLE** -Struktur an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.

Das **Children** -Element der [**vs \_ VERSIONINFO**](vs-versioninfo.md) -Struktur kann NULL oder mehr **stringfileinfo** -Strukturen enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**STRINGTABLE**](stringtable.md)
</dt> <dt>

[**Schnür**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





