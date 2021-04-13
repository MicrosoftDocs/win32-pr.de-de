---
title: kurzes Attribut
description: Das Short-Schlüsselwort legt eine 16-Bit-Ganzzahl fest.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- kurzes Attribut-Mittel l
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312743"
---
# <a name="short-attribute"></a>kurzes Attribut

Das **Short** -Schlüsselwort legt eine 16-Bit-Ganzzahl fest.

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dem **Short** -Schlüsselwort kann entweder das Schlüsselwort [**signiert**](signed.md) oder das Schlüsselwort [**unsigniert**](unsigned.md)vorangestellt werden. Das [**int**](int.md) -Schlüsselwort ist optional und kann ausgelassen werden. Für den mittlerer l-Compiler ist standardmäßig eine kurze Ganzzahl signiert und mit einem **Signed short int**-Wert Synonym.

Der **kurze ganzzahlige** Typ ist einer der Basis Typen der IDL-Sprache. Der **kurze ganzzahlige** Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabetyp-Spezifizierer und Parameter-Typspezifizierer) vorkommen. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**ebenes**](signed.md)
</dt> <dt>

[**zuletzt**](small.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> </dl>

 

 




