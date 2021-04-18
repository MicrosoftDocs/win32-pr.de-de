---
title: vararg-Attribut
description: Das Attribut \ vararg \ gibt an, dass die Funktion eine Variable Anzahl von Parametern annimmt. Um dies zu erreichen, muss der letzte Parameter ein sicheres Array vom Variant-Typ sein, das alle verbleibenden Parameter enthält.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- vararg-Attribut-Mittel l
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337224"
---
# <a name="vararg-attribute"></a>vararg-Attribut

Das **\[ vararg \]** -Attribut gibt an, dass die Funktion eine Variable Anzahl von Parametern annimmt. Um dies zu erreichen, muss der letzte Parameter ein sicheres Array vom **Variant** -Typ sein, das alle verbleibenden Parameter enthält.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*optionale Attribute* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die auf die Funktion angewendet werden sollen. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Typ der Daten, die von der Remote Prozedur nach Abschluss des Vorgangs zurückgegeben werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name der Remote Prozedur.

</dd> <dt>

*optional-param-Attribute* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die auf den Funktionsparameter direkt nach der Attribut Auflistung angewendet werden sollen.

</dd> <dt>

*param-Liste* 
</dt> <dd>

Gibt alle Parameter an, speichert den abschließenden, variierenden Parameter.

</dd> <dt>

*Last-Param-Name* 
</dt> <dd>

Der Name des variierenden Parameters.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\[** [**optionalen**](optional.md) **\]** Attribute oder **\[** [**DefaultValue**](defaultvalue.md) -Attribute können nicht **\]** auf Parameter in einer Funktion angewendet werden, die das **\[ \] vararg** -Attribut aufweist.

## <a name="examples"></a>Beispiele

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**optionale**](optional.md)
</dt> </dl>

 

 