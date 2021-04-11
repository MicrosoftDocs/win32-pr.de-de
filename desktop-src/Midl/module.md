---
title: Module-Attribut
description: Die Module-Anweisung definiert eine Gruppe von Funktionen, in der Regel einen Satz von dll-Einstiegspunkten.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- Modul Attribut-Mittel l
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314877"
---
# <a name="module-attribute"></a>Module-Attribut

Die **Module** -Anweisung definiert eine Gruppe von Funktionen, in der Regel einen Satz von dll-Einstiegspunkten.

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

Die \[ Attribute [**UUID**](uuid.md) \] , \[ [**Version**](version.md) \] , \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] und \[ [**dllName**](dllname-str-.md) \] werden vor einer **Modul** Anweisung akzeptiert. Weitere Informationen zu den Attributen, die vor einer Modul Definition akzeptiert werden, finden Sie unter [Attribut Beschreibungen](/previous-versions/windows/desktop/automat/attribute-descriptions)im OLE-Automatisierungs Buch. Das \[ **dllName** - \] Attribut ist erforderlich. Wenn das \[ **UUID** - \] Attribut weggelassen wird, wird das Modul im System nicht eindeutig angegeben.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Der Name des Moduls.

</dd> <dt>

*Elementliste* 
</dt> <dd>

Liste konstanter Definitionen und Funktionsprototypen für jede Funktion in der dll. Eine beliebige Anzahl von Funktionsdefinitionen kann in der Funktionsliste angezeigt werden. Eine Funktion in der Funktionsliste weist die folgende Form auf:

\[*Attribute* \] *returnType* \[ funkname der Aufruf *Konvention* \] (*para* Metern);

\[*Attribute* \] [**const**](const.md) constanttype *constname*  =  *constval*;

Nur die \[ [**HelpString**](helpstring.md) \] -und \[ [**HelpContext**](helpcontext.md) - \] Attribute werden für einen [**Konstanten**](const.md)akzeptiert.

Die folgenden Attribute werden für eine Funktion in einem Modul akzeptiert: \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**Entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**PROPPUT**](propput.md) \] , \[ [**PROPPUTREF**](propputref.md) \] und \[ [**vararg**](vararg.md) \] . Wenn \[ **vararg** \] angegeben ist, muss der letzte Parameter ein sicheres Array vom **Variant** -Typ sein.

Die optionale Aufruf Konvention kann " \_ \_ Pascal/ \_ Pascal/Pascal", " \_ \_ cdecl/ \_ cdecl/cdecl" oder " \_ \_ StdCall/ \_ StdCall/stdcall" lauten. Der *Typ paramName der Aufruf Konvention* kann bis zu zwei führende Unterstriche enthalten.

Die Parameterliste ist eine durch Trennzeichen getrennte Liste von:

\[*legt*\]

Der Typ kann ein beliebiger zuvor deklarierter Typ oder integrierter Typ, ein Zeiger auf einen beliebigen Typ oder ein Zeiger auf einen integrierten Typ sein. Attribute für Parameter sind:

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**optional**](optional.md) \] .

Wenn \[ [**optional**](optional.md) \] verwendet wird, müssen die Typen dieser Parameter **Variant** oder Variant sein  \* .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Ausgabe der Header Datei (. h) für Module ist eine Reihe von Funktionsprototypen. Das Schlüsselwort " **Module** " und die umgebenden Klammern werden aus der Ausgabe der Header Datei (. h) entfernt, es wird jedoch ein Kommentar (// **Modul Modul** *Name*) vor den Prototypen eingefügt. Das Schlüsselwort **extern** wird vor den Deklarationen eingefügt.

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

[**dllname**](dllname-str-.md)
</dt> <dt>

[**ein**](entry.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**verbirgt**](hidden.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 