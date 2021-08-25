---
title: StringFileInfo-Struktur
description: Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- StringFileInfo-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e130090c7281f6ef61ed0a3a82b822863bb5c12ff1194e26b07a70467db82cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720830"
---
# <a name="stringfileinfo-structure"></a>StringFileInfo-Struktur

Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.

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

**wLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Länge des gesamten **StringFileInfo-Blocks** in Bytes, einschließlich aller strukturen, die durch den **Children-Member** angegeben werden.

</dd> <dt>

**wValueLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Dieser Member ist immer gleich 0 (null).

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

Die Unicode-Zeichenfolge L"StringFileInfo".

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

So viele 0 Wörter wie erforderlich, um das **Children-Element** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **[ **StringTable**](stringtable.md)**

</dd> <dd>

Ein Array von einer oder mehreren [**StringTable-Strukturen.**](stringtable.md) Der **szKey-Member** jeder **StringTable-Struktur** gibt die entsprechende Sprache und Codepage für die Anzeige des Texts in dieser **StringTable-Struktur** an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist keine echte C-Sprachstruktur, da sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versionsressource erstellt und wird in keiner der Headerdateien angezeigt, die mit dem Windows Software Development Kit (SDK) ausgeliefert werden.

Der **Children-Member** der [**VS \_ VERSIONINFO-Struktur**](vs-versioninfo.md) kann 0 (null) oder mehr **StringFileInfo-Strukturen** enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





