---
title: MENUEX-Ressource
description: Definiert den Inhalt einer Menüressource. | MENUEX-Ressource
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- MENUEX-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec78bd0d33b48b11de77fe7742affb4265160752ffad30d72ecf3e9c173bb77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825940"
---
# <a name="menuex-resource"></a>MENUEX-Ressource

Definiert den Inhalt einer Menüressource. Eine Menüressource ist eine Sammlung von Informationen, die die Darstellung und Funktion eines Anwendungsmenüs definieren. Ein Menü ist ein spezielles Eingabetool, mit dem ein Benutzer Befehle auswählen und Untermenüs aus einer Liste von Menüelementen öffnen kann. Außerdem wird Folgendes definiert:

-   Hilfebezeichner in Menüs.
-   Bezeichner in Menüs.
-   Verwendung der *\_ \* *MFT_-Typflags* und _*\_ \* MFS-Zustandsflags.*_ Weitere Informationen zu diesen Flags finden Sie in der [*_MENUITEMINFO-Struktur.* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**Menuitem**](menuitem-statement.md)
</dt> <dd>

Definiert ein Menüelement.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Eine Zeichenfolge, die den Text für das Menüelement enthält. Weitere Informationen finden Sie unter [**MENUITEM**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Numerischer Ausdruck, der den Bezeichner des Menüelements angibt.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Typ*
</dt> <dd>

Numerischer Ausdruck, der den Typ des Menüelements angibt. Um die vordefinierten MFT-Typwerte zu verwenden, schließen Sie die folgende Anweisung \_ \* in die RC-Datei ein:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Staat*
</dt> <dd>

Numerischer Ausdruck, der den Zustand des Menüelements angibt. Um die vordefinierten MFS-Statuswerte zu verwenden, schließen Sie die \_ \* folgende Anweisung in Ihre ein. RC-Datei:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**Popup**](popup-resource.md)
</dt> <dd>

Definiert ein Menüelement, dem ein Untermenü zugeordnet ist.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Eine Zeichenfolge, die den Text für das Menüelement enthält.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Numerischer Ausdruck, der den Bezeichner des Menüelements angibt.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Typ*
</dt> <dd>

Numerischer Ausdruck, der den Typ des Menüelements angibt Um die vordefinierten MFT-Typwerte zu verwenden, schließen Sie die \_ \* folgende Anweisung in Ihre ein. RC-Datei:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Staat*
</dt> <dd>

Numerischer Ausdruck, der den Status des Menüelements angibt: Fügen Sie die folgende Anweisung \_ in die RC-Datei ein. Um die vordefinierten MFS-Statuswerte \* zu verwenden:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Numerischer Ausdruck, der den Bezeichner angibt, mit dem das Menü während der [**WM \_ HELP-Verarbeitung identifiziert**](../shell/wm-help.md) wird.

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Enthält eine beliebige Kombination der [**MENUITEM- und**](menuitem-statement.md) [**POPUP-Anweisungen.**](popup-resource.md)

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="remarks"></a>Hinweise

Die gültigen arithmetischen und booleschen Operationen, die in einem der numerischen Ausdrücke in den **MENUEX-Anweisungen** enthalten sein können, lauten wie folgt:

-   Hinzufügen ('+')
-   Subtrahieren ('-')
-   Unäres Minus ("-")
-   Unär NOT ('~')
-   AND ('&')
-   OR (' \| ')

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Menüs](./using-menus.md)
</dt> <dt>

[**Beschleuniger**](accelerators-resource.md)
</dt> <dt>

[**Merkmale**](characteristics-statement.md)
</dt> <dt>

[**DIALOG**](dialog-resource.md)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Menuitem**](menuitem-statement.md)
</dt> <dt>

[**Popup**](popup-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 
