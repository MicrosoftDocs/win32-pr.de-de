---
title: char-Attribut
description: Das Char-Schlüsselwort gibt ein 8-Bit-Datenelement an.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- char-Attribut-Mittel l
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857592"
---
# <a name="char-attribute"></a>char-Attribut

Das **char** -Schlüsselwort gibt ein 8-Bit-Datenelement an.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Schlüsselwort **char** identifiziert ein Datenelement, das über 8 Bits verfügt. Für den mittlerer l-Compiler ist ein **char** standardmäßig **unsigniert und** mit Vorzeichen [**ohne**](unsigned.md) Vorzeichen Synonym.

In dieser Version von Microsoft RPC werden die Zeichen Übersetzungstabellen, die zwischen ASCII und EBCDIC konvertiert werden, in die Laufzeitbibliotheken integriert und können vom Benutzer nicht geändert werden.

Der **char** -Typ ist einer der Basis Typen der IDL (Interface Definition Language). Der **char** -Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabetyp-Spezifizierer und Parameter-Typspezifizierer) vorkommen. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

DCE-IDL-Compiler akzeptieren das auf **char** - [**Typen angewendete**](signed.md) Schlüsselwort nicht. Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Hobby**](byte.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




