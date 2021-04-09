---
title: Optionales Attribut
description: Das \ optionale \-Attribut gibt einen optionalen Parameter für eine Member-Funktion an.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- optionales Attribut-Mittel l
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858239"
---
# <a name="optional-attribute"></a>Optionales Attribut

Das **\[ optionale \]** -Attribut gibt einen optionalen Parameter für eine Member-Funktion an.

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*andere-Attribute* 
</dt> <dd>

NULL oder mehr optionale Mittelwert Attribute.

</dd> <dt>

*Parametertyp* 
</dt> <dd>

Der Datentyp des optionalen Parameters.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt den Namen des optionalen Parameters an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ optionale \]** -Attribut ist nur gültig, wenn der-Parameter vom Typ **Variant** oder **Variant** ist \* .

Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter, die nicht über das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut oder **\[ optionale \]** Attribute verfügen)
2.  Optionale Parameter mit oder ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut
3.  Parameter mit dem **\[ optionalen \]** -Attribut und ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut
4.  **\[**[**LCID**](lcid.md) - **\]** Parameter (falls vorhanden)
5.  **\[**[**retval**](retval.md) **\]** Parame

Sie können das **\[ \] optionale** -Attribut nicht auf einen Parameter anwenden, der auch über die **\[** [**LCID**](lcid.md) - **\]** oder **\[** [**retval**](retval.md) -Attribute verfügt **\]** .

## <a name="examples"></a>Beispiele

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 