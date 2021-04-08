---
title: hyperattribute
description: Das Schlüsselwort hypergibt eine 64-Bit-Ganzzahl an, die als "signiert" oder "nicht signiert" deklariert werden kann.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- hyperattributmittell
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718071"
---
# <a name="hyper-attribute"></a>hyperattribute

Das Schlüsselwort **hypergibt** eine 64-Bit-Ganzzahl an, die als "signiert" oder "nicht signiert" deklariert werden kann.

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren. (Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig. Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **hypertyp** ist einer der Basis Typen der IDL (Interface Definition Language). Der **hypertyp** kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Für 16-Bit-Plattformen ersetzt der mittlerer l-Compiler nicht signierte hyperintegerwerte durch die **mittlere \_** benutzerdefinierte Funktion. Dadurch können Schnittstellen mit nicht signierten hyperintegern auf Plattformen definiert werden, die keine direkte Unterstützung von 64-Bit-Ganzzahlen aufweisen. Die **mittlere \_** benutzerdefinierte Funktion ist in den RPC-Header Dateien definiert.

 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




