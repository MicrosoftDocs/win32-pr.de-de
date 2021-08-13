---
title: vararg-Attribut
description: Das \fgrg\-Attribut gibt an, dass die Funktion eine variable Anzahl von Parametern verwendet. Um dies zu erreichen, muss der letzte Parameter ein sicheres Array vom Typ VARIANT sein, das alle verbleibenden Parameter enthält.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- MIDL-Attribut des fgrg-Attributs
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848393f6bad82d6793e34ba6f4da803c7dd64803c1c40e4ea05487ea141ec48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641008"
---
# <a name="vararg-attribute"></a>vararg-Attribut

Das **\[ Attribut \] fgrg** gibt an, dass die Funktion eine variable Anzahl von Parametern verwendet. Um dies zu erreichen, muss der letzte Parameter ein sicheres Array vom **Typ VARIANT** sein, das alle verbleibenden Parameter enthält.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optional-attributes* 
</dt> <dd>

Gibt null oder mehr Attribute an, die auf die Funktion angewendet werden sollen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*return-type* 
</dt> <dd>

Der Typ der Daten, die nach Abschluss der Remoteprozedur zurückgegeben werden.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name der Remoteprozedur.

</dd> <dt>

*optional-param-attributes* 
</dt> <dd>

Gibt null oder mehr Attribute an, die unmittelbar nach der Attributauflistung auf den Funktionsparameter angewendet werden sollen.

</dd> <dt>

*param-list* 
</dt> <dd>

Gibt alle Parameter an, und speichern Sie den endgültigen, variierenden Parameter.

</dd> <dt>

*last-param-name* 
</dt> <dd>

Der Name des variierenden Parameters.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können die **\[** [**optionalen attribute oder**](optional.md) defaultvalue-Attribute nicht auf Parameter in einer Funktion anwenden, die **\]** über das Attribut **\[** [](defaultvalue.md) **\]** **\[ fgrg \]** verfügt.

## <a name="examples"></a>Beispiele

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Defaultvalue**](defaultvalue.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Optional**](optional.md)
</dt> </dl>

 

 