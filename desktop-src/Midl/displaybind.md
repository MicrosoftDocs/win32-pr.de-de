---
title: displaybind-Attribut
description: Das Attribut \displaybind\ gibt eine Eigenschaft an, die dem Benutzer als bindbar angezeigt werden soll.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- displaybind attribute MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f331ee62128501237671d01524c0f74df5ebc3b9da37dbf6ba3f71f9a5df460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384604"
---
# <a name="displaybind-attribute"></a>displaybind-Attribut

Das **\[ displaybind-Attribut \]** gibt eine Eigenschaft an, die dem Benutzer als bindbar angezeigt werden soll.

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

*interface-attribute-list* 
</dt> <dd>

Gibt eine optionale Liste von Schnittstellenattributen an.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt eine Durch Kommas getrennte Liste von Attributen an, die für den Funktions-Rückgabetyp gelten.

</dd> <dt>

*returntype* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ displaybind-Attribut \]** angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameterliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eigenschaften, die über das **\[ displaybind-Attribut \]** verfügen, müssen auch über das **\[** [**bindbare Attribut**](bindable.md) **\]** verfügen. Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.

### <a name="flags"></a>Flags

FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND

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

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 