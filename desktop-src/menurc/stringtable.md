---
title: StringTable-Struktur
description: Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält Sprach- und Codepageformatierungsinformationen für die Vom Untergeordneten Element angegebenen Zeichenfolgen. Eine Codepage ist ein geordneter Zeichensatz.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- StringTable-StrukturMenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01ad7a2436c4b32f0f2fa09ab801339903ed55f35be80bbfc43c4542da4e4ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720660"
---
# <a name="stringtable-structure"></a>StringTable-Struktur

Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält Sprach- und Codepageformatierungsinformationen für die Vom **Untergeordneten** Element angegebenen Zeichenfolgen. Eine Codepage ist ein geordneter Zeichensatz.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a>Member

<dl> <dt>

**wLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Länge dieser **StringTable-Struktur** in Bytes, einschließlich aller strukturen, die durch den **Children-Member** angegeben werden.

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

Eine achtstellige Hexadezimalzahl, die als Unicode-Zeichenfolge gespeichert ist. Die vier signifikantesten Ziffern stellen den Sprachbezeichner dar. Die vier am wenigsten signifikanten Ziffern stellen die Codepage dar, für die die Daten formatiert sind. Jeder Microsoft Standard Language-Bezeichner enthält zwei Teile: Die 10 Bits mit niedriger Reihenfolge geben die Hauptsprache an, und die 6 Bits mit hoher Ordnung geben die Untersprache an. Eine Tabelle gültiger Bezeichner finden Sie unter .

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

So viele 0 Wörter wie erforderlich, um das **Children-Element** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **[ **Zeichenfolge**](string-str.md)**

</dd> <dd>

Ein Array von einer oder mehreren [**Zeichenfolgenstrukturen.**](string-str.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist keine echte C-Sprachstruktur, da sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versionsressource erstellt und wird in keiner der Headerdateien angezeigt, die mit dem Windows Software Development Kit (SDK) ausgeliefert werden.

Der **Children-Member** der [**StringFileInfo-Struktur**](stringfileinfo.md) enthält mindestens eine **StringTable-Struktur.**

Legen Sie den Codepageteil des **szKey-Elements** auf den Hexadezimalwert 0x04b0 fest, um die Unicode-Codepage anzugeben, oder auf den Hexadezimalwert der Codepage, der für die Sprachkomponente geeignet ist. Nachdem Sie den Wert für die Codepage ausgewählt haben, sollten Sie in späteren Revisionen der Datei weiterhin denselben Wert verwenden.

Eine ausführbare Datei oder DLL, die mehrere Sprachen unterstützt, sollte über eine Versionsressource für jede Sprache verfügen, anstatt über eine einzelne Versionsressource, die Zeichenfolgen in mehreren Sprachen enthält. Wenn Sie jedoch die [**Var-Struktur**](var-str.md) verwenden, um die Sprachen aufzulisten, die ihre Anwendung unterstützt, hängt die Anzahl der **StringTable-Strukturen** in der Versionsressource direkt mit der Anzahl der Sprachen-/Codepagebezeichnerpaare im **Value-Member** der **Var-Struktur** zusammen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





