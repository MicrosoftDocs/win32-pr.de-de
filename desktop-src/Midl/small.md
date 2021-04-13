---
title: Small-Attribut
description: Das Small-Schlüsselwort gibt eine 8-Bit-Ganzzahl an.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- Small Attribute-Mittel l
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389002"
---
# <a name="small-attribute"></a>Small-Attribut

Das **Small** -Schlüsselwort gibt eine 8-Bit-Ganzzahl an.

``` syntax
small identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dem **Small** -Schlüsselwort kann entweder das Schlüsselwort [**signiert**](signed.md) oder das Schlüsselwort [**unsigniert**](unsigned.md)vorangestellt werden. Das [**int**](int.md) -Schlüsselwort ist optional und kann ausgelassen werden. Für den mittlerer l-Compiler ist standardmäßig eine kleine Ganzzahl **signiert** und ist mit dem Wert " **Signed Small int**" Synonym.

Der **kleine** ganzzahlige Typ ist einer der Basis Typen der IDL-Sprache. Der **Small** Integer-Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabe –-Typspezifizierer und als Parametertyp Spezifizierer) vorkommen. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

Das Vorzeichen des **kleinen** Typs kann mit dem Mittell-Compilerschalter [**/char**](-char.md)geändert werden. Um Verwirrung zu vermeiden, geben Sie das Vorzeichen des ganzzahligen Typs mit den Schlüsselwörtern [**signiert**](signed.md) und [**unsigniert**](unsigned.md)an.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




