---
title: STRINGTABLE-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält sprach-und Code Page Formatierungsinformationen für die Zeichen folgen, die vom Children-Member angegeben werden. Eine Codepage ist ein geordneter Zeichensatz.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- STRINGTABLE-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391653"
---
# <a name="stringtable-structure"></a>STRINGTABLE-Struktur

Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält sprach-und Code Page Formatierungsinformationen für die Zeichen folgen, die vom **Children** -Member angegeben werden. Eine Codepage ist ein geordneter Zeichensatz.

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

**wlength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge der **STRINGTABLE** -Struktur in Bytes, einschließlich aller **vom untergeordneten** Element angegeben Strukturen.

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

Eine 8-stellige hexadezimal Zahl, die als Unicode-Zeichenfolge gespeichert wird. Die vier signifikantesten Ziffern stellen den sprach Bezeichner dar. Die vier wichtigsten Ziffern stellen die Codepage dar, für die die Daten formatiert sind. Jeder Bezeichner der Microsoft-Standard Sprache enthält zwei Teile: die nieder wertigen 10 Bits geben die Hauptsprache an, und die höherwertigen 6 Bits geben die unter Sprache an. Eine Tabelle gültiger Bezeichner finden Sie unter.

</dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **Word**

</dd> <dd>

So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Children**
</dt> <dd>

Typ: **[ **Zeichenfolge**](string-str.md)**

</dd> <dd>

Ein Array aus einer oder mehreren [**Zeichen**](string-str.md) folgen Strukturen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.

Der **Children** -Member der [**stringfileinfo**](stringfileinfo.md) -Struktur enthält mindestens eine **STRINGTABLE** -Struktur.

Legen Sie den Codepage-Teil des **szkey** -Members auf den Hexadezimalwert 0x04b0 fest, um die Unicode-Codepage anzugeben, oder auf den Hexadezimalwert der Codepage, der für die Sprachkomponente geeignet ist. Nachdem Sie den Wert für die Codepage ausgewählt haben, sollten Sie den gleichen Wert auch in späteren Revisionen der Datei verwenden.

Eine ausführbare Datei oder dll, die mehrere Sprachen unterstützt, sollte über eine Versions Ressource für jede Sprache verfügen, anstatt über eine einzige Versions Ressource, die Zeichen folgen in mehreren Sprachen enthält. Wenn Sie jedoch die [**var**](var-str.md) -Struktur verwenden, um die Sprachen aufzulisten, die von der Anwendung unterstützt werden, ist die Anzahl der **STRINGTABLE** -Strukturen in der Versions Ressource direkt mit der Anzahl der sprach-/Codepage-bezeichnerpaare im **Wertmember** der **var** -Struktur verknüpft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Schnür**](string-str.md)
</dt> <dt>

[**Stringfileingefo**](stringfileinfo.md)
</dt> <dt>

[**Kreis**](var-str.md)
</dt> <dt>

[**Varfileingefo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





