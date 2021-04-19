---
title: Bindbares Attribut
description: Das \ Bindable \-Attribut gibt an, dass die-Eigenschaft die Datenbindung unterstützt.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- bindbares Attribut, Mittel l
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341711"
---
# <a name="bindable-attribute"></a>Bindbares Attribut

Das **\[ bindbare \]** Attribut gibt an, dass die Eigenschaft die Datenbindung unterstützt.

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

*Interface-Attribute-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für den Funktionsprototyp für eine Eigenschaft oder eine Methode in einer [**Schnittstelle**](interface.md) oder einem [**dispinterface**](dispinterface.md)-Objekt gelten. Die folgenden Attribute sind gültig: [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ String \]**](string.md), [**\[ Defaultbind \]**](defaultbind.md), [**\[ Display Bind \]**](displaybind.md), [**\[ \] unmittelatebind**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ PROPPUT \]**](propput.md), [**\[ PROPPUTREF \]**](propputref.md)und [**\[ vararg \]**](vararg.md). Wenn **vararg** angegeben ist, muss der letzte Parameter ein sicheres Array vom Typ Variant sein. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die das **\[ bindbare \]** Attribut angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameter Liste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Durch die Unterstützung der Datenbindung ermöglicht das **\[ bindbare \]** Attribut dem Client, immer dann benachrichtigt zu werden, wenn eine Eigenschaft den Wert geändert hat. (Wenn Sie möchten, dass der Client über bevorstehende Änderungen an einer Eigenschaft benachrichtigt wird, verwenden Sie das [**\[ requestedit \]**](requestedit.md) -Attribut.)

Da das **\[ bindbare \]** Attribut auf die Eigenschaft als Ganzes verweist, muss es immer dann angegeben werden, wenn die Eigenschaft definiert ist. Daher müssen Sie das-Attribut für die Eigenschaften Zugriffs Funktion und die-Eigenschaft festlegen.

### <a name="flags"></a>Flags

funcflag \_ FBindable, varflag \_ FBindable

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

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 