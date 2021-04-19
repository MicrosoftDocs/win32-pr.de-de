---
title: Resourceheader-Struktur
description: Enthält Informationen über den Ressourcen Header selbst und die Daten, die für diese Ressource spezifisch sind.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Resourceheader-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342188"
---
# <a name="resourceheader-structure"></a>Resourceheader-Struktur

Enthält Informationen über den Ressourcen Header selbst und die Daten, die für diese Ressource spezifisch sind. Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**DataSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe (in Bytes) der Daten, die dem Ressourcen Header für diese bestimmte Ressource folgen. Es enthält keine Datei Auffüll Zeichen zwischen dieser Ressource und einer beliebigen Ressource in der Ressourcen Datei.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der folgenden Ressourcen Header Daten in Bytes.

</dd> <dt>

**TYPE**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Ressourcentyp. Der **Typmember** kann entweder ein numerischer Wert oder eine auf NULL endende Unicode-Zeichenfolge sein, die den Namen des Typs angibt. Im folgenden Abschnitt "Hinweise" finden Sie eine Beschreibung der Member des Typs " **Name** " oder " **Ordinal** ".

Wenn der **Typmember** ein numerischer Wert ist, kann er entweder einen Standard-oder einen benutzerdefinierten Ressourcentyp angeben. Wenn der Member eine Zeichenfolge ist, ist es ein benutzerdefinierter Ressourcentyp. Eine Liste der vordefinierten Ressourcentypen finden Sie unter [Ressourcentypen](/windows/desktop/menurc/resource-types).

Werte kleiner als 256 sind für die Verwendung durch das System reserviert.

</dd> <dt>

**NAME**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein Name, der die jeweilige Ressource identifiziert. Das **Name** -Element kann wie der **Typmember** entweder ein numerischer Wert oder eine auf NULL endende Unicode-Zeichenfolge sein. Im folgenden Abschnitt "Hinweise" finden Sie eine Beschreibung der Member des Typs " **Name** " oder " **Ordinal** ".

Sie müssen keine Auffüll Zeichen für die **DWORD** -Ausrichtung zwischen den **Typen** -und **namens** Elementen hinzufügen, da Sie **Word** -Daten enthalten. Sie müssen jedoch möglicherweise nach dem **Name** -Element ein **Wort** zum Auffüllen hinzufügen, um den Rest des Headers an **DWORD** -Grenzen auszurichten.

</dd> <dt>

**DataVersion**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Eine vordefinierte Ressourcen Daten Version. Dadurch wird festgelegt, welche Version der Ressourcen Daten von der Anwendung verwendet werden soll.

</dd> <dt>

**Memoryflags**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein Satz von Attributflags, die den Zustand der Ressource beschreiben können. Modifiziererer in. RC-Skriptdatei weisen Sie diese Attribute der Ressource zu. Die Skript Bezeichner können die folgenden Flagwerte zuweisen.

Anwendungen verwenden keines dieser Attribute. Die Attribute sind im Skript für die Abwärtskompatibilität mit vorhandenen Skripts zulässig, werden jedoch ignoriert. Ressourcen werden geladen, wenn das entsprechende Modul geladen wird, und werden freigegeben, wenn das Modul entladen wird.

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**Verschiebbare** (0x0010)


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

**korrigiert** (~-fähig)


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**Pure** (0x0020)


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**Impure** (~ Pure)


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**Vorab laden** (0x0040)


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL(** ~ preload)


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

**Verwerfen** (0x1000)


</dt> <dd></dd> </dl> </dd> <dt>

**LanguageID**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Sprache für die Ressource oder den Satz von Ressourcen. Legen Sie den Wert für diesen Member mit der optionalen [Language](./language-statement.md) Resource Definition-Anweisung fest. Die Parameter sind Konstanten aus der Datei "Winnt. h".

Jede Ressource enthält eine sprach Kennung, damit das System oder die Anwendung eine Sprache auswählen kann, die für das aktuelle Gebiets Schema des Systems geeignet ist. Wenn mehrere Ressourcen desselben Typs und Namens vorhanden sind, die sich nur in der Sprache der Zeichen folgen innerhalb der Ressourcen unterscheiden, müssen Sie für jeden eine **LanguageID** angeben.

</dd> <dt>

**Version**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Eine benutzerdefinierte Versionsnummer für die Ressourcen Daten, die Tools zum Lesen und Schreiben von Ressourcen Dateien verwenden können. Legen Sie diesen Wert mit der optionalen [Version](./version-statement.md) Resource Definition-Anweisung fest.

</dd> <dt>

**Characteristics**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt benutzerdefinierte Informationen über die Ressource an, die Tools zum Lesen und Schreiben von Ressourcen Dateien verwenden können. Legen Sie diesen Wert mit der optionalen [Merkmale](./characteristics-statement.md) Resource Definition-Anweisung fest.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein variablentypmember wird als **Name** oder **ordinalmember** bezeichnet und wird an den meisten Stellen in der Ressourcen Datei verwendet, in der ein Bezeichner angezeigt wird. Das erste **Wort** eines **namens** oder eines **ordinaltypmembers** gibt an, ob der Member ein numerischer Wert oder eine Zeichenfolge ist. Wenn das erste **Wort** im Member gleich dem Wert 0xFFFF ist, bei dem es sich um ein ungültiges Unicode-Zeichen handelt, ist das folgende **Wort** eine Typnummer. Andernfalls enthält der Member eine Unicode-Zeichenfolge, und das erste **Wort** im Member ist das erste Zeichen in der namens Zeichenfolge. Weitere Informationen zu Ressourcen Definitions Anweisungen finden Sie unter [Ressourcen Definitions Anweisungen](./resource-definition-statements.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Merkmale-Anweisung](./characteristics-statement.md)
</dt> <dt>

[Language-Anweisung](./language-statement.md)
</dt> <dt>

[Versions Anweisung](./version-statement.md)
</dt> </dl>

 

