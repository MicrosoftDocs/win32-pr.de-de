---
title: STRINGTABLE-Ressource
description: Definiert mindestens eine Zeichenfolgenressourcen für eine Anwendung. Zeichenfolgenressourcen sind einfach auf NULL terminierte Unicode- oder ASCII-Zeichenfolgen, die bei Bedarf mithilfe der LoadString-Funktion aus der ausführbaren Datei geladen werden können.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- STRINGTABLE-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7994b6853195ba164c766ca6ee275e4535ab1249c0c78907ab996b9dc644013a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720650"
---
# <a name="stringtable-resource"></a>STRINGTABLE-Ressource

Definiert mindestens eine Zeichenfolgenressourcen für eine Anwendung. Zeichenfolgenressourcen sind einfach auf NULL terminierte Unicode- oder ASCII-Zeichenfolgen, die bei Bedarf mithilfe der [**LoadString-Funktion**](/windows/win32/api/winuser/nf-winuser-loadstringa) aus der ausführbaren Datei geladen werden können.

Es gibt zwei Möglichkeiten, eine **STRINGTABLE-Anweisung zu** formatieren:

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- oder –

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Dieser Parameter kann null oder mehr der folgenden Anweisungen sein.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [](characteristics-statement.md) *CHARACTERISTICS-DWORD*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden können, die Ressourcendateien lesen und schreiben. Weitere Informationen finden Sie unter [**CHARACTERISTICS**](characteristics-statement.md). |
| [](language-statement.md) *LANGUAGE-Sprache,* *Untersprache* | Gibt die Sprache für die Ressource an. Weitere Informationen finden Sie unter [**LANGUAGE**](language-statement.md).                                                                              |
| [**VERSIONSdword**](version-statement.md)                      | Benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcendateien lesen und schreiben. Weitere Informationen finden Sie unter [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*Schnur*
</dt> <dd>

Mindestens eine Zeichenfolge, die in Anführungszeichen eingeschlossen ist. Die Zeichenfolge darf nicht länger als 4097 Zeichen sein und muss eine einzelne Zeile in der Quelldatei belegen. Um der Zeichenfolge einen Wagenrücklauf hinzuzufügen, verwenden Sie diese Zeichenfolge: \\ 012. Beispielsweise definiert "Zeile \\ eins 012Linie zwei" eine Zeichenfolge, die wie folgt angezeigt wird:

``` syntax
Line one
Line two
```

Verwenden Sie die folgende Sequenz, um Anführungszeichen in die Zeichenfolge einbetten: "". Beispielsweise definiert """Zeile 3""" eine Zeichenfolge, die wie folgt angezeigt wird:

``` syntax
"Line three"
```

Verwenden Sie zum Codieren von Unicode-Zeichen ein "L", gefolgt von den Unicode-Zeichen, die in Anführungszeichen eingeschlossen sind. Ein Beispiel finden Sie im Abschnitt Beispiele.

Der Ressourcencompiler unterstützt auch Zeilenfortsetzungen in der *Zeichenfolge*. Ein Beispiel finden Sie im Abschnitt Beispiele.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="remarks"></a>Hinweise

RC ordnet 16 Zeichenfolgen pro Abschnitt zu und verwendet den Bezeichnerwert, um zu bestimmen, welcher Abschnitt die Zeichenfolge enthalten soll. Zeichenfolgen, deren Bezeichner sich nur in den unteren 4 Bits unterscheiden, werden im gleichen Abschnitt platziert. Weitere Informationen finden Sie unter [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **STRINGTABLE-Anweisung** zum Anzeigen von ASCII-Zeichenfolgen veranschaulicht:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

Das folgende Beispiel zeigt, wie Unicode-Zeichen codiert werden:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

Das folgende Beispiel zeigt Zeichenfolgen mit ASCII und Unicode. Beachten Sie, dass Zeichenfolgen ohne das anfängliche "L" das 2-stellige Escapeformat verwenden:

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

Das folgende Beispiel zeigt, wie Zeilenfortsetzungen verwendet werden können:

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**Beschleuniger**](accelerators-resource.md)
</dt> <dt>

[**Merkmale**](characteristics-statement.md)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 