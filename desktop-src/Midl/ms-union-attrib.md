---
title: ms_union-Attribut
description: Das Schlüsselwort \ms \_ union\ wird verwendet, um die NDR-Ausrichtung von nicht gekapselten Unions zu steuern.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union-Attribut MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 860054fe26657c4028c172da08e0c56dbf6ae257ffc98e79905f8420b54e6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642798"
---
# <a name="ms_union-attribute"></a>ms \_ union-Attribut

Das Schlüsselwort \[ **ms \_ union** \] wird verwendet, um die NDR-Ausrichtung von nicht gekapselten Unions zu steuern.

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

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*prozedur-type* 
</dt> <dd>

Gibt den Rückgabetyp der Prozedur an, auf die das Attribut angewendet wird.

</dd> <dt>

*Prozedurname* 
</dt> <dd>

Gibt den Namen der Prozedur an.

</dd> <dt>

*param-list* 
</dt> <dd>

Gibt die Parameterliste der Prozedur an, die leer sein kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diesen Schalter oder dieses Attribut niemals mit neuen Schnittstellen. Dies ist nur ein Abwärtskompatibilitätsfeature. Der MIDL-Compiler in dieser Version von Microsoft RPC spiegelt das Verhalten des OSF DCE-IDL-Compilers für nicht gekapselte Unions wider. Da frühere Versionen des MIDL-Compilers dies jedoch nicht getan haben, bietet der [**\_ /ms-Union-Switch**](-ms-union.md) Kompatibilität mit Schnittstellen, die auf früheren Versionen des MIDL-Compilers basierten.

Das **feature ms \_ union** kann als IDL-Schnittstellenattribut, als IDL-Typattribut oder als Befehlszeilenschalter ( [**/ms \_ union**](-ms-union.md)) verwendet werden.

## <a name="examples"></a>Beispiele

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**/ms \_ union**](-ms-union.md)
</dt> </dl>

 

 




