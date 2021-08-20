---
title: Bindbares Attribut
description: Das Attribut \bindable\gibt an, dass die -Eigenschaft die Datenbindung unterstützt.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- BINDABLE-Attribut MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a673c696a810856b6c520680898e4f48e6cb5e5ed108a22f8ecd1132383416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807863"
---
# <a name="bindable-attribute"></a>Bindbares Attribut

Das **\[ bindbare Attribut \]** gibt an, dass die -Eigenschaft die Datenbindung unterstützt.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr IDL-Attributen an, die für die Schnittstelle als Ganzes gelten. Wenn mindestens zwei Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für den Funktionsprototyp für eine Eigenschaft oder eine Methode in einer Schnittstelle oder [**Dispinterface gelten.**](dispinterface.md) [](interface.md) Die folgenden Attribute sind gültig: [**\[ \] helpstring**](helpstring.md), [**\[ helpcontext \]**](helpcontext.md), [**\[ \] string**](string.md), [**\[ defaultbind \]**](defaultbind.md), displaybind , [**\[ \] immediatebind**](displaybind.md) [**\[ \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)und [**\[ triburg \]**](vararg.md). Wenn **fgrg angegeben** wird, muss der letzte Parameter ein sicheres Array vom Typ VARIANT sein. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*returntype* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ bindbare \]** Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameterliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Durch die Unterstützung der Datenbindung ermöglicht das **\[ bindbare \]** Attribut dem Client, benachrichtigt zu werden, wenn eine Eigenschaft den Wert geändert hat. (Wenn Sie möchten, dass der Client über bevorstehende Änderungen an einer Eigenschaft benachrichtigt wird, verwenden Sie das [**\[ \] requestedit-Attribut.)**](requestedit.md)

Da das **\[ bindbare Attribut \]** auf die Eigenschaft als Ganzes verweist, muss es überall dort angegeben werden, wo die Eigenschaft definiert ist. Daher müssen Sie das -Attribut sowohl für die Eigenschaftszugriffsfunktion als auch für die Eigenschaftseinstellungsfunktion angeben.

### <a name="flags"></a>Flags

FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**Propput**](propput.md)
</dt> <dt>

[**Propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 