---
title: cpp_quote-Attribut
description: Das \_ cpp quote-Schlüsselwort weist MIDL an, die angegebene Zeichenfolge ohne anführungszeichen in der generierten Headerdatei auszugeben.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote-Attribut MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaef6b765834dfbbe1def90fa6d0d2596998514e32ddeb8107978838f8debd6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991608"
---
# <a name="cpp_quote-attribute"></a>\_CPP-Anführungszeichenattribut

Das **cpp \_** quote-Schlüsselwort weist MIDL an, die angegebene Zeichenfolge ohne anführungszeichen in der generierten Headerdatei auszugeben.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string* 
</dt> <dd>

Gibt eine Zeichenfolge in Anführungszeichen an, die in der generierten Headerdatei ausgegeben wird. Die Zeichenfolge muss in Anführungszeichen geschrieben werden, um eine Erweiterung durch den C-Präprozessor zu verhindern.

</dd> </dl>

## <a name="remarks"></a>Hinweise

C-Sprachvorverarbeitungsdirektiven, die in der IDL-Datei angezeigt werden, werden vom Präprozessor des C-Compilers verarbeitet. Die **\# define-Direktiven** in der IDL-Datei sind während der MIDL-Kompilierung verfügbar, aber nicht für den C-Compiler verfügbar.

Wenn der Präprozessor beispielsweise auf die Anweisung \# "windows 4 definieren" trifft, ersetzt der Präprozessor alle Vorkommen von "WINDOWS" in der IDL-Datei durch "4". Das Symbol "WINDOWS" ist während der C-Sprachkompilierung nicht verfügbar.

Damit die C-Präprozessormakrodefinitionen den MIDL-Compiler an den C-Compiler übergeben können, verwenden Sie die **\# pragma midl \_ echo-** oder **cpp-Anführungszeichendirektive. \_** Diese Anweisungen weisen den MIDL-Compiler an, eine Headerdatei zu generieren, die die Parameterzeichenfolge mit den entfernten Anführungszeichen enthält. Die **\# Pragma-Anweisungen midl \_ echo** und **cpp \_ quote** sind gleichwertig.

Der MIDL-Compiler platziert die in den **CPP-Anführungszeichen \_** und [**Pragmaanweisungen**](pragma.md) angegebenen Zeichenfolgen in der Headerdatei in der Sequenz, in der sie in der IDL-Datei angegeben sind, und relativ zu anderen Schnittstellenkomponenten in der IDL-Datei. Die Zeichenfolgen sollten in der Regel nach allen [**Importvorgängen**](import.md) im Textabschnitt der IDL-Dateischnittstelle angezeigt werden.

## <a name="examples"></a>Beispiele

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**import**](import.md)
</dt> <dt>

[**Pragma**](pragma.md)
</dt> </dl>

 

 




