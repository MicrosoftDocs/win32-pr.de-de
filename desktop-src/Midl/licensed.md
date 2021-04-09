---
title: licensed-Attribut
description: Das Attribut \ lizenzierte \ gibt an, dass die Co-Klasse, auf die es angewendet wird, lizenziert ist und mit IClassFactory2 instanziiert werden muss.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- lizenzierte Attribute-Mittel l
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038859"
---
# <a name="licensed-attribute"></a>licensed-Attribut

Das **\[ lizenzierte \]** Attribut gibt an, dass die [**Co-Klasse**](coclass.md) , auf die Sie angewendet wird, lizenziert ist und mit [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)instanziiert werden muss.

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die [**Co-Klasse**](coclass.md) -Anweisung gelten. Zulässige **Co-Klasse** -Attribute sind **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ lizenziert \]**, **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** und **\[** [**Hidden**](hidden.md) **\]** .

</dd> <dt>

*classname* 
</dt> <dd>

Gibt den Namen an, mit dem das Komponenten Objekt in der Typbibliothek bekannt ist.

</dd> <dt>

*coclass-Definition* 
</dt> <dd>

Gibt die-Anweisungen an, die die [**Co-Klassen**](coclass.md) Definition bilden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Lizenzierung ist eine Funktion von com, die die Kontrolle über die Objekt Erstellung ermöglicht. Lizenzierte Objekte können nur von Clients erstellt werden, die zur Verwendung autorisiert sind. Die Lizenzierung wird in com über die [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) -Schnittstelle und durch Unterstützung eines Lizenzschlüssels implementiert, der zur Laufzeit übermittelt werden kann.

### <a name="flags"></a>Flags

TYPEFLAG \_ geflichtet

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Inhalt einer Typbibliothek](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Steuerelement**](control.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**verbirgt**](hidden.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 