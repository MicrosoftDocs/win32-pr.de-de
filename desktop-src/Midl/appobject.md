---
title: appobject-Attribut
description: Das Attribut \ appobject \ identifiziert die Co-Klasse als Anwendungs Objekt, das einer vollständigen exe-Anwendung zugeordnet ist.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject-Attribut-Mittel l
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390201"
---
# <a name="appobject-attribute"></a>appobject-Attribut

Das **\[ appobject \]** -Attribut identifiziert die [**Co-Klasse**](coclass.md) als Anwendungs Objekt, das einer vollständigen exe-Anwendung zugeordnet ist.

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

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die [**Co-Klasse**](coclass.md)an.

</dd> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die [**Co-Klasse**](coclass.md) -Anweisung gelten. Zulässige **Co-Klasse** -Attribute sind [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ lizenziert \]**](licensed.md), [**\[ Version \]**](version.md), [**\[ Control \]**](control.md)und [**\[ Hidden \]**](hidden.md).

</dd> <dt>

*classname* 
</dt> <dd>

Gibt den Namen an, mit dem das Komponenten Objekt in der Typbibliothek bekannt ist.

</dd> <dt>

*Co-Klassendefinition* 
</dt> <dd>

Gibt die-Anweisungen an, die die [**Co-Klassen**](coclass.md) Definition bilden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ appobject \]** -Attribut gibt auch an, dass die Funktionen und Eigenschaften der [**Co-Klasse**](coclass.md) in der aktuellen Typbibliothek global verfügbar sind.

Die TYPEFLAG-Darstellung für dieses Attribut ist "TYPEFLAG \_ fappobject".

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

[**lizenziert**](licensed.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 