---
title: cpp_quote-Attribut
description: Das cpp- \_ Anführungszeichen Schlüsselwort weist die Mittel l an, die angegebene Zeichenfolge ohne Anführungszeichen in die generierte Header Datei auszugeben.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote Attribut-Mittel l
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038110"
---
# <a name="cpp_quote-attribute"></a>cpp- \_ Anführungszeichen Attribut

Das **cpp- \_ Anführungs** Zeichen Schlüsselwort weist die Mittel l an, die angegebene Zeichenfolge ohne Anführungszeichen in die generierte Header Datei auszugeben.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string* 
</dt> <dd>

Gibt eine Zeichenfolge in Anführungszeichen an, die in der generierten Header Datei ausgegeben wird. Die Zeichenfolge muss in Anführungszeichen eingeschlossen werden, um zu verhindern, dass der C-Präprozessor

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In der IDL-Datei angezeigte Vorverarbeitung-Direktiven der c-Sprache werden vom Präprozessor des C-Compilers verarbeitet. Die **\# define** -Direktiven in der IDL-Datei sind während der Mitte der Kompilierung verfügbar, sind aber für den C-Compiler nicht verfügbar.

Wenn der Präprozessor z. b. auf die Direktive " \# Windows 4 definieren" stößt, ersetzt der Präprozessor alle Vorkommen von "Windows" in der IDL-Datei durch "4". Das Symbol "Windows" ist während der Kompilierung der C-Sprache nicht verfügbar.

Um zuzulassen, dass die c-präprozessormakrodefinitionen den Mittel l-Compiler an den c-Compiler übergeben, verwenden Sie die- **\# pragma \_** -Anweisung "-Echo" oder " **cpp- \_ Anführungs** Zeichen". Diese Direktiven weisen den Mittelwert Compiler an, eine Header Datei zu generieren, die die Parameter Zeichenfolge enthält, wobei die Anführungszeichen entfernt werden. Die Anweisungs-und **cpp- \_** Anweisungs Direktiven von **\# pragma \_** sind gleichwertig.

Der mittlerer l-Compiler fügt die in den **cpp- \_ Anführungs** Zeichen und- [**pragma**](pragma.md) -Direktiven angegebenen Zeichen folgen in die Header Datei in der Reihenfolge, in der Sie in der IDL-Datei angegeben sind, und relativ zu anderen Schnittstellen Komponenten in der IDL-Datei ein. Die Zeichen folgen sollten in der Regel im Textabschnitt der IDL-Datei Schnittstelle nach allen [**Import**](import.md) Vorgängen angezeigt werden.

## <a name="examples"></a>Beispiele

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Importieren**](import.md)
</dt> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




