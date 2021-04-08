---
title: Long-Attribut
description: Das Long-Schlüsselwort gibt eine 32-Bit-Ganzzahl an.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- Long-Attribut-Mittel l
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948165"
---
# <a name="long-attribute"></a>Long-Attribut

Das **Long** -Schlüsselwort gibt eine 32-Bit-Ganzzahl an.

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dem **Long** -Schlüsselwort kann entweder das Schlüsselwort [**signiert**](signed.md) oder das Schlüsselwort [**unsigniert**](unsigned.md)vorangestellt werden. Das [**int**](int.md) -Schlüsselwort ist optional und kann ausgelassen werden. Für den mittlerer l-Compiler ist eine lange ganze Zahl standardmäßig signiert und mit **Signed long int** Synonym. Auf 32-Bit-Plattformen ist **Long** gleichbedeutend mit **int**.

Der **Long** Integer-Typ ist einer der Basis Typen der IDL-Sprache. Der **Long** Integer-Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabe –-Typspezifizierer und als Parametertyp Spezifizierer) vorkommen. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Hyper**](hyper.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**zuletzt**](small.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> </dl>

 

 




