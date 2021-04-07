---
title: displaybind-Attribut
description: Das Attribut \ displaybind \ gibt eine Eigenschaft an, die dem Benutzer als Bindable angezeigt werden soll.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- Display BIND-Attribut (Mittell)
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725433"
---
# <a name="displaybind-attribute"></a>displaybind-Attribut

Das **\[ Display Bind \]** -Attribut gibt eine Eigenschaft an, die dem Benutzer als Bindable angezeigt werden soll.

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine optionale Liste der Schnittstellen Attribute an.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den Funktions Rückgabetyp angewendet werden.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ Display Bind \]** -Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameter Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eigenschaften, die über das **\[ Display Bind \]** -Attribut verfügen, müssen auch über das **\[** [**bindbare**](bindable.md) **\]** Attribut verfügen. Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.

### <a name="flags"></a>Flags

funcflag " \_ f Display BIND", varflag " \_ sbind"

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 