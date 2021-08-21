---
title: pragma-Attribut
description: Die \pragma midl echo-Direktive weist MIDL an, die angegebene Zeichenfolge ohne anführungszeichen in die \_ generierte Headerdatei ausgibt.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma attribute MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ca869acddf4b0a0a098707833e889efcfccc267a3abf1949921c550cf66c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383498"
---
# <a name="pragma-attribute"></a>pragma-Attribut

Die \# **pragma midl \_ echo-Direktive** weist MIDL an, die angegebene Zeichenfolge ohne anführungszeichen in die generierte Headerdatei ausgibt.

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

Gibt eine Zeichenfolge an, die in die generierte Headerdatei eingefügt wird. Die Anführungszeichen werden während des Einfügevorgangs entfernt.

</dd> <dt>

*Tokensequenz* 
</dt> <dd>

Gibt eine Sequenz von Token an, die als Teil einer **\# Pragma-Direktive** ohne Verarbeitung durch den MIDL-Compiler in die generierte Headerdatei eingefügt werden.

</dd> <dt>

*n* 
</dt> <dd>

Gibt die aktuelle Paketgröße an. Gültige Werte sind 1, 2, 4, 8 und 16.

</dd> <dt>

*id* 
</dt> <dd>

Gibt die Benutzer-ID an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

C-Sprachvorverarbeitungsdirektiven, die in der IDL-Datei angezeigt werden, werden vom Präprozessor des C-Compilers verarbeitet. Die **\# define-Direktiven** in der IDL-Datei sind während der MIDL-Kompilierung verfügbar, jedoch nicht für den C-Compiler.

Wenn der Präprozessor beispielsweise auf die Direktive "WINDOWS 4 definieren" trifft, ersetzt der Präprozessor alle Vorkommen von "WINDOWS" in der IDL-Datei durch \# "4". Das Symbol "WINDOWS" ist zur C-Kompilierungszeit nicht verfügbar.

Damit die C-Präprozessormakrodefinitionen den MIDL-Compiler an den C-Compiler übergeben können, verwenden Sie die **\# pragma midl \_ echo-** oder [**cpp \_ quote-Direktive.**](cpp-quote.md) Diese Anweisungen weisen den MIDL-Compiler an, eine Headerdatei zu generieren, die die Parameterzeichenfolge mit den entfernten Anführungszeichen enthält. Die **\# pragma midl \_ echo- und** **cpp \_ quote-Direktiven** sind gleichwertig.

Die **\# pragma pack-Direktive** wird vom MIDL-Compiler verwendet, um das Packen von Strukturen zu steuern. Er überschreibt den [**Befehlszeilenschalter /Zp.**](-zp.md) Die Paketoption (*n*) legt die aktuelle Paketgröße auf einen bestimmten Wert fest: 1, 2, 4, 8 oder 16. Die Optionen pack (push) und pack (pop) haben die folgenden Merkmale:

-   Der Compiler verwaltet einen Packstapel. Die Elemente des Paketstapels enthalten eine Paketgröße und eine optionale *ID.* Der Stapel ist nur durch den verfügbaren Arbeitsspeicher mit der aktuellen Paketgröße am anfang des Stapels beschränkt.
-   Das Packen (Pushen) führt zu der aktuellen Paketgröße, die auf den Paketstapel pusht. Der Stapel ist durch den verfügbaren Arbeitsspeicher beschränkt.
-   Pack (push,*n*) ist identisch mit pack (push) gefolgt von pack (*n*).
-   Pack (push, *id*) *pusht* id zusammen mit der Paketgröße ebenfalls auf den Paketstapel.
-   Pack (push, *id*, *n*) ist identisch mit pack (push, *id*) gefolgt von pack (*n*).
-   Packen (Pop) führt zum Popen des Paketstapels. Unausgeglichene Pops verursachen Warnungen und legen die aktuelle Paketgröße auf den Befehlszeilenwert fest.
-   Wenn pack (pop, *id,* *n*) angegeben wird, wird *n* ignoriert.

Der MIDL-Compiler platziert die in den [**\\ Anweisungen cpp \_ quote**](cpp-quote.md) und **pragma** angegebenen Zeichenfolgen in der Headerdatei in der Sequenz, in der sie in der IDL-Datei angegeben sind, und relativ zu anderen Schnittstellenkomponenten in der IDL-Datei. Die Zeichenfolgen sollten in der Regel nach allen Importvorgängen im Abschnitt interface-body der IDL-Datei [**angezeigt**](import.md) werden.

Der MIDL-Compiler versucht nicht, **\# Pragma-Direktiven** zu verarbeiten, die nicht mit dem Präfix "midl" \_ beginnen. Andere **\# Pragma-Direktiven** in der IDL-Datei werden ohne Änderungen an die generierte Headerdatei übergeben.

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

[**\_CPP-Anführungszeichen**](cpp-quote.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**import**](import.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




