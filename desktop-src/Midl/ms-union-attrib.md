---
title: ms_union-Attribut
description: Das Schlüsselwort \ MS \_ Union \ wird zum Steuern der NDR-Ausrichtung von nicht gekapselten Unions verwendet.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- Ms_union Attribut-Mittel l
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037816"
---
# <a name="ms_union-attribute"></a>MS- \_ Union-Attribut

Das Schlüsselwort " \[ **MS \_ Union** " \] wird zum Steuern der NDR-Ausrichtung von nicht gekapselten Unions verwendet.

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Prozedurtyp* 
</dt> <dd>

Gibt den Rückgabetyp der Prozedur an, auf die das Attribut angewendet wird.

</dd> <dt>

*Prozedur Name* 
</dt> <dd>

Gibt den Namen der Prozedur an.

</dd> <dt>

*param-Liste* 
</dt> <dd>

Gibt die Parameterliste der Prozedur an, die möglicherweise leer ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diesen Switch oder dieses Attribut niemals mit neuen Schnittstellen. Dies ist nur ein abwärts Kompatibilitäts Feature. Der mittlerer l-Compiler in dieser Version von Microsoft RPC spiegelt das Verhalten des OSF-DCE-IDL-Compilers für nicht gekapselte Unions wider. Da jedoch frühere Versionen des Mittel l-Compilers dies nicht getan haben, bietet der [**/MS \_ Union**](-ms-union.md) -Switch Kompatibilität mit Schnittstellen, die auf früheren Versionen des Mittel l-Compilers erstellt wurden.

Die **MS- \_ Union** -Funktion kann als idl-Schnittstellen Attribut, IDL-Typattribut oder als Befehls Zeilenschalter ( [**/MS \_ Union**](-ms-union.md)) verwendet werden.

## <a name="examples"></a>Beispiele

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/MS- \_ Union**](-ms-union.md)
</dt> </dl>

 

 




