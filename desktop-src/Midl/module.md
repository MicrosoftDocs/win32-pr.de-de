---
title: Modulattribut
description: Die Modul-Anweisung definiert eine Gruppe von Funktionen, in der Regel einen Satz von DLL-Einstiegspunkten.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- Midl-Modulattribut
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642808"
---
# <a name="module-attribute"></a>Modulattribut

Die **Modul-Anweisung** definiert eine Gruppe von Funktionen, in der Regel einen Satz von DLL-Einstiegspunkten.

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*attributes* 
</dt> <dd>

Die Attribute \[ [**uuid**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helpstring**](helpstring.md), \] \[ [**helpcontext**](helpcontext.md), \] \[ [**hidden**](hidden.md) \] und \[ [**dllname**](dllname-str-.md) werden vor einer \] Modulanweisung akzeptiert.  Weitere Informationen zu den Attributen, die vor einer Moduldefinition akzeptiert werden, finden Sie unter [Attributbeschreibungen](/previous-versions/windows/desktop/automat/attribute-descriptions)im Buch OLE-Automatisierung. Das \[ **attribut dllname** \] ist erforderlich. Wenn das \[ **uuid-Attribut** \] ausgelassen wird, wird das Modul im System nicht eindeutig angegeben.

</dd> <dt>

*Modulename* 
</dt> <dd>

Der Name des Moduls.

</dd> <dt>

*elementlist* 
</dt> <dd>

Liste der konstanten Definitionen und Funktionsprototypen für jede Funktion in der DLL. Eine beliebige Anzahl von Funktionsdefinitionen kann in der Funktionsliste angezeigt werden. Eine Funktion in der Funktionsliste hat die folgende Form:

\[*Attribute* \] *returntype* \[ *calling convention funcname* \] (*params*);

\[*Attribute* \] [**const**](const.md) constanttype *constname*  =  *constval*;

Nur die \[ [**Attribute helpstring**](helpstring.md) \] und \[ [**helpcontext**](helpcontext.md) werden für eine \] [**const**](const.md)akzeptiert.

Die folgenden Attribute werden für eine Funktion in einem Modul akzeptiert: \[ [**helpstring**](helpstring.md) \] , \[ [**helpcontext**](helpcontext.md) \] , \[ [**string**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md), \] \[ [**propput**](propput.md), \] \[ [**propputref**](propputref.md)und \] \[ [**lvarg**](vararg.md) \] . Wenn \[ **lvarg** \] angegeben wird, muss der letzte  Parameter ein sicheres Array vom Variant-Typ sein.

Die optionale Aufrufkonvention kann eine von \_ \_ \_ "pascal/pascal/pascal", \_ \_ "cdecl/cdecl/cdecl" \_ oder \_ \_ "stdcall/stdcall/stdcall" \_ sein. Der *Aufrufkonventionentyp paramname* kann bis zu zwei führende Unterstriche enthalten.

Die Parameterliste ist eine durch Kommas getrennte Liste von:

\[*Attribute*\]

Der Typ kann ein beliebiger zuvor deklarierter Typ oder integrierter Typ, ein Zeiger auf einen beliebigen Typ oder ein Zeiger auf einen integrierten Typ sein. Attribute für Parameter sind:

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**optional.**](optional.md) \]

Wenn \[ [**optional**](optional.md) \] verwendet wird, müssen die Typen dieser Parameter **VARIANT** oder **VARIANT** \* sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Ausgabe der Headerdatei (.h) für Module ist eine Reihe von Funktionsprototypen. Das **Modulschlüsselwort** und die umgebenden Klammern werden aus der Headerdateiausgabe (.h) entfernt, aber vor den Prototypen wird ein Kommentar (/ **Modulmodulname** ) eingefügt. Das Schlüsselwort **extern** wird vor den Deklarationen eingefügt.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Inhalt einer Typbibliothek](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Eintrag**](entry.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Versteckte**](hidden.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**Propput**](propput.md)
</dt> <dt>

[**Propputref**](propputref.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 