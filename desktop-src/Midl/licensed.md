---
title: licensed-Attribut
description: Das Attribut \licensed\ gibt an, dass die Co-Klasse, für die sie gilt, lizenziert ist und mit IClassFactory2 instanziiert werden muss.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- lizenziertes Attribut MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4320157216db18f595d67e172bc49de2d6050551732265060cb5a21339c908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067206"
---
# <a name="licensed-attribute"></a>licensed-Attribut

Das **\[ lizenzierte Attribut \]** gibt an, dass die [**Co-Klasse,**](coclass.md) für die es gilt, lizenziert ist und mit [**IClassFactory2 instanziiert werden muss.**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)

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

*Attributliste* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die [**coclass-Anweisung gelten.**](coclass.md) Zulässige **Co-Klasse-Attribute** sind **\[** [**helpstring,**](helpstring.md) **\]** **\[** [**helpcontext,**](helpcontext.md) **\]** **\[ lizenziert, \]** **\[** [**version,**](version.md) **\]** **\[** [**control**](control.md)und **\]** **\[** [**hidden.**](hidden.md) **\]**

</dd> <dt>

*classname* 
</dt> <dd>

Gibt den Namen an, unter dem das Komponentenobjekt in der Typbibliothek bekannt ist.

</dd> <dt>

*coclass-definition* 
</dt> <dd>

Gibt Anweisungen an, aus denen sich die [**Co-Klasse-Definition**](coclass.md) zusammengibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Lizenzierung ist ein Feature von COM, das die Kontrolle über die Objekterstellung bietet. Lizenzierte Objekte können nur von Clients erstellt werden, die für deren Verwendung autorisiert sind. Die Lizenzierung wird in COM über die [**IClassFactory2-Schnittstelle**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) und durch Unterstützung eines Lizenzschlüssels implementiert, der zur Laufzeit übergeben werden kann.

### <a name="flags"></a>Flags

TYPEFLAG \_ FLICENSED

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

[**Steuerung**](control.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**Versteckte**](hidden.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 