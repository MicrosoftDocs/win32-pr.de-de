---
title: boolesches Attribut
description: Das Schlüsselwort boolescher Wert gibt an, dass der Ausdruck oder konstanter Ausdruck, der mit dem Bezeichner verknüpft ist, nur die Werte true und false annimmt.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- boolesches Attribut, Mittel l
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389224"
---
# <a name="boolean-attribute"></a>boolesches Attribut

Das Schlüsselwort **boolescher** Wert gibt an, dass der Ausdruck oder konstanter Ausdruck, der mit dem Bezeichner verknüpft ist, nur die Werte **true** und **false** annimmt.

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **boolesche** Typ ist einer der Basis Typen der IDL-Sprache. Der **boolesche** Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Der **boolesche** Basistyp ist nicht kompatibel mit dem [**oleautomation**](oleautomation.md) -Attribut. Verwenden \_ Sie Variant bool in ihren Automation-kompatiblen Schnittstellen.

 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




