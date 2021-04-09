---
title: STRINGTABLE-Ressource
description: Definiert eine oder mehrere Zeichen folgen Ressourcen für eine Anwendung. Zeichen folgen Ressourcen sind einfach mit NULL endende Unicode-oder ASCII-Zeichen folgen, die bei Bedarf aus der ausführbaren Datei mithilfe der LoadString-Funktion geladen werden können.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- STRINGTABLE-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101627"
---
# <a name="stringtable-resource"></a>STRINGTABLE-Ressource

Definiert eine oder mehrere Zeichen folgen Ressourcen für eine Anwendung. Zeichen folgen Ressourcen sind einfach mit NULL endende Unicode-oder ASCII-Zeichen folgen, die bei Bedarf aus der ausführbaren Datei mithilfe der [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) -Funktion geladen werden können.

Es gibt zwei Möglichkeiten, eine **STRINGTABLE** -Anweisung zu formatieren:

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- oder -

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

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*
</dt> <dd>

Dieser Parameter kann NULL oder mehr der folgenden-Anweisungen sein.



| -Anweisung.                                                        | BESCHREIBUNG                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Merkmale**](characteristics-statement.md) *DWORD*     | Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md). |
| [**Sprach**](language-statement.md) *Sprache*, *unter Sprache* | Gibt die Sprache für die Ressource an. Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).                                                                              |
| [**Version**](version-statement.md) *DWORD*                     | Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben. Weitere Informationen finden Sie unter [**Version**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*Schnür*
</dt> <dd>

Eine oder mehrere Zeichen folgen, die in Anführungszeichen eingeschlossen sind. Die Zeichenfolge darf nicht länger als 4097 Zeichen sein und muss eine einzelne Zeile in der Quelldatei belegen. Um der Zeichenfolge einen Wagen Rücklauf hinzuzufügen, verwenden Sie diese Zeichenfolge: \\ 012. Beispiel: "Line One \\ 012line Two" definiert eine Zeichenfolge, die wie folgt angezeigt wird:

``` syntax
Line one
Line two
```

Um Anführungszeichen in die Zeichenfolge einzubetten, verwenden Sie die folgende Sequenz: "". Beispielsweise wird in "" in Zeile drei "" "eine Zeichenfolge definiert, die wie folgt angezeigt wird:

``` syntax
"Line three"
```

Um Unicode-Zeichen zu codieren, verwenden Sie eine "L", gefolgt von den in Anführungszeichen eingeschlossenen Unicode-Zeichen. Ein Beispiel finden Sie im Abschnitt "Beispiele".

Der Ressourcen Compiler unterstützt auch Zeilen Fortsetzungen in der *Zeichenfolge*. Ein Beispiel finden Sie im Abschnitt "Beispiele".

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

RC ordnet 16 Zeichen folgen pro Abschnitt zu und verwendet den Bezeichnerwert, um zu bestimmen, welcher Abschnitt die Zeichenfolge enthalten soll. Zeichen folgen, deren Bezeichner sich nur in den unteren 4 Bits unterscheiden, werden im gleichen Abschnitt platziert. Weitere Informationen finden Sie unter [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht die Verwendung der **STRINGTABLE** -Anweisung zum Anzeigen von ASCII-Zeichen folgen:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

Im folgenden Beispiel wird gezeigt, wie Unicode-Zeichen codiert werden:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

Das folgende Beispiel zeigt Zeichen folgen mit ASCII und Unicode. Beachten Sie, dass Zeichen folgen ohne das ursprüngliche "L" das zweistellige escapeformat verwenden:

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

Im folgenden Beispiel wird gezeigt, wie Zeilen Fortsetzungen verwendet werden können:

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 