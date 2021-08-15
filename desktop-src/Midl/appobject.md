---
title: appobject-Attribut
description: Das Attribut \appobject\ identifiziert die Co-Klasse als Anwendungsobjekt, das einer vollständigen EXE-Anwendung zugeordnet ist.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject-Attribut MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54cbe8d5c1c7a573216ae9cb55075ba3b3766d0d8c7898233be9364488131e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808332"
---
# <a name="appobject-attribute"></a>appobject-Attribut

Das **\[ attribut \] appobject** identifiziert die [**Co-Klasse**](coclass.md) als Anwendungsobjekt, das einer vollständigen EXE-Anwendung zugeordnet ist.

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die [**Co-Klasse an.**](coclass.md)

</dd> <dt>

*coclass-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die [**coclass-Anweisung gelten.**](coclass.md) Zulässige **Co-Klasse-Attribute** sind [**\[ \] helpstring,**](helpstring.md) [**\[ helpcontext, \]**](helpcontext.md) [**\[ lizenziert, \]**](licensed.md) [**\[ version, \]**](version.md) [**\[ control \]**](control.md)und [**\[ hidden. \]**](hidden.md)

</dd> <dt>

*classname* 
</dt> <dd>

Gibt den Namen an, unter dem das Komponentenobjekt in der Typbibliothek bekannt ist.

</dd> <dt>

*Co-Klasse-Definition* 
</dt> <dd>

Gibt Anweisungen an, aus denen sich die [**Co-Klasse-Definition**](coclass.md) zusammengibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ attribut \] appobject** gibt auch an, dass die Funktionen und Eigenschaften der [**Co-Klasse**](coclass.md) global in der aktuellen Typbibliothek verfügbar sind.

Die Typflagdarstellung für dieses Attribut ist TYPEFLAG \_ FAPPOBJECT.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
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

[**Lizenziert**](licensed.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 