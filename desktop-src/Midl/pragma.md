---
title: pragma-Attribut
description: Die Anweisung \ Pragma Mittel l \_ Echo weist die angegebene Zeichenfolge ohne Anführungszeichen in der generierten Header Datei an.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma-Attribut-Mittel l
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948125"
---
# <a name="pragma-attribute"></a>pragma-Attribut

Mit der Pragma-Anweisung "-Echo" wird die \# angegebene Zeichenfolge (ohne Anführungszeichen) in der generierten Header Datei durch die-Anweisung des- **pragma \_** -Attributs ausgegeben.

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string* 
</dt> <dd>

Gibt eine Zeichenfolge an, die in die generierte Header Datei eingefügt wird. Die Anführungszeichen werden während des Einfügevorgangs entfernt.

</dd> <dt>

*tokensequenz* 
</dt> <dd>

Gibt eine Sequenz von Token an, die in die generierte Header Datei als Teil einer **\# pragma** -Direktive eingefügt werden, ohne dass vom Mittelwert Compiler verarbeitet wird.

</dd> <dt>

*n* 
</dt> <dd>

Gibt die aktuelle Paketgröße an. Gültige Werte sind 1, 2, 4, 8 und 16.

</dd> <dt>

*id* 
</dt> <dd>

Gibt die Benutzer-ID an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In der IDL-Datei angezeigte Vorverarbeitung-Direktiven der c-Sprache werden vom Präprozessor des C-Compilers verarbeitet. Die **\# define** -Direktiven in der IDL-Datei sind während der Kompilierungs Kompilierung verfügbar, aber nicht für den C-Compiler.

Wenn der Präprozessor z. b. auf die Direktive " \# Windows 4 definieren" stößt, ersetzt der Präprozessor alle Vorkommen von "Windows" in der IDL-Datei durch "4". Das Symbol "Windows" ist zum Zeitpunkt der C-Kompilierung nicht verfügbar.

Um zuzulassen, dass die c-präprozessormakrodefinitionen den Mittel l-Compiler an den c-Compiler übergeben, verwenden Sie die- **\# pragma \_** -Anweisung "-Echo" oder " [**cpp- \_ Anführungs**](cpp-quote.md) Zeichen". Diese Direktiven weisen den Mittelwert Compiler an, eine Header Datei zu generieren, die die Parameter Zeichenfolge enthält, wobei die Anführungszeichen entfernt werden. Die Anweisungs-und **cpp- \_** Anweisungs Direktiven von **\# pragma \_** sind gleichwertig.

Die **\# pragma pack** -Direktive wird vom Mittelwert Compiler zum Steuern der Verpackung von Strukturen verwendet. Er überschreibt den [**/ZP**](-zp.md) -Befehls Zeilenschalter. Die Option Pack (*n*) legt die aktuelle Paketgröße auf einen bestimmten Wert fest: 1, 2, 4, 8 oder 16. Die Optionen Pack (Push) und Pack (Pop) weisen die folgenden Eigenschaften auf:

-   Der Compiler behält einen Verpackungs Stapel bei. Die Elemente des Verpackungs Stapels enthalten eine Paketgröße und eine optionale *ID*. Der Stapel wird nur durch den verfügbaren Arbeitsspeicher mit der aktuellen Paketgröße am oberen Rand des Stapels beschränkt.
-   Pack (Push) führt dazu, dass die aktuelle Paketgröße auf den Verpackungs Stapel verschoben wird. Der Stapel ist durch den verfügbaren Arbeitsspeicher begrenzt.
-   Pack (Push,*n*) ist das gleiche wie Pack (Push), gefolgt von Pack (*n*).
-   Pack (Push, *ID*) überträgt ebenfalls die *ID* zusammen mit der Paketgröße auf den Verpackungs Stapel.
-   Pack (Push, *ID*, *n*) ist das gleiche wie Pack (Push, *ID*), gefolgt von Paket (*n*).
-   Pack (Pop) führt zu einem Pop in den Verpackungs Stapel. Unausgeglichene POPs verursachen Warnungen und legen die aktuelle Paketgröße auf den Befehlszeilen Wert fest.
-   Wenn Pack (Pop, *ID*, *n*) angegeben wird, wird *n* ignoriert.

Der-compilercompiler fügt die in den [**\\ cpp- \_ Anführungs**](cpp-quote.md) Zeichen und- **pragma** -Direktiven angegebenen Zeichen folgen in der-Header Datei in der Reihenfolge ein, in der Sie in der IDL-Datei und relativ zu anderen Schnittstellen Komponenten in der IDL-Datei angegeben sind. Die Zeichen folgen sollten in der Regel im Schnittstellen Textabschnitt der IDL-Datei nach allen [**Import**](import.md) Vorgängen angezeigt werden.

Der mittlerer l-Compiler versucht nicht, **\# pragma** -Direktiven zu verarbeiten, die nicht mit dem Präfix "Mittel l \_ " beginnen. Andere **\# pragma** -Direktiven in der IDL-Datei werden ohne Änderungen an die generierte Header Datei übermittelt.

## <a name="examples"></a>Beispiele

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**cpp- \_ Angebot**](cpp-quote.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Importieren**](import.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




