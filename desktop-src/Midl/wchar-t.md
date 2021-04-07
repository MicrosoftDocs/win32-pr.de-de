---
title: wchar_t-Attribut
description: Das WCHAR \_ t-Schlüsselwort legt einen breit Zeichentyp fest.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t Attribut-Mittel l
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "104038648"
---
# <a name="wchar_t-attribute"></a>WCHAR \_ t-Attribut

Das **WCHAR \_ t** -Schlüsselwort legt einen breit Zeichentyp fest.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen Mittell-Bezeichner an. Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Typ " **WCHAR \_ t** " wird von "Mittel l" als [**unsigniertes**](unsigned.md) [**kurzes**](short.md) (16-Bit-) Datenobjekt definiert.

Der mittlerer l-Compiler lässt die Neudefinition von **WCHAR \_ t** zu, jedoch nur, wenn er mit der vorangehenden Definition konsistent ist.

Der breit Zeichentyp ist einer der vordefinierten Typen von "Mittel l". Der breit Zeichentyp kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

Das **\[ String \]** -Attribut kann auf einen Zeiger oder ein Array vom Typ " **WCHAR \_ t**" angewendet werden.

Verwenden Sie das **L** -Zeichen vor einem Zeichen oder einer Zeichen folgen Konstante, um die Konstante für den breit Zeichentyp festzulegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> </dl>

 

 




