---
title: Menuex-Ressource
description: Definiert den Inhalt einer Menü Ressource. | Menuex-Ressource
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menuex-Ressourcen Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363100"
---
# <a name="menuex-resource"></a>Menuex-Ressource

Definiert den Inhalt einer Menü Ressource. Eine Menü Ressource ist eine Auflistung von Informationen, die das Aussehen und die Funktion eines Anwendungs Menüs definiert. Ein Menü ist ein spezielles Eingabe Tool, mit dem ein Benutzer Befehle auswählen und Untermenüs aus einer Liste von Menü Elementen öffnen kann. Außerdem wird Folgendes definiert:

-   Hilfe Bezeichner in Menüs.
-   Bezeichner in Menüs.
-   Verwendung der **MFT \_ \** _-Typflags und _*MFS \_ \**_ -Statusflags. Weitere Informationen zu diesen Flags finden Sie in der [_ *menuiteminfo* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur.

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

Definiert ein Menü Element.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*ItemText*
</dt> <dd>

Zeichenfolge, die den Text für das Menü Element enthält. Weitere Informationen finden Sie unter [**MenuItem**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Numerischer Ausdruck, der den Bezeichner des Menü Elements angibt.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Sorte*
</dt> <dd>

Numerischer Ausdruck, der den Typ des Menü Elements angibt, für das die vordefinierten MFT- \_ \* Typwerte verwendet werden sollen. Fügen Sie die folgende Anweisung in die RC-Datei ein:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Land*
</dt> <dd>

Numerischer Ausdruck, der den Zustand des Menü Elements angibt, in dem die vordefinierten MFS- \_ \* Zustands Werte verwendet werden sollen. Fügen Sie die folgende Anweisung in den ein. RC-Datei:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**Up**](popup-resource.md)
</dt> <dd>

Definiert ein Menü Element, das über ein zugeordnetes Untermenü verfügt.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*ItemText*
</dt> <dd>

Zeichenfolge, die den Text für das Menü Element enthält.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Numerischer Ausdruck, der den Bezeichner des Menü Elements angibt.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Sorte*
</dt> <dd>

Numerischer Ausdruck, der den Typ des Menü Elements angibt, für das die vordefinierten MFT- \_ \* Typwerte verwendet werden sollen. Fügen Sie die folgende Anweisung in ihr ein. RC-Datei:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Land*
</dt> <dd>

Numerischer Ausdruck, der den Zustand des Menü Elements angibt, in dem die vordefinierten MFS- \_ \* Zustands Werte verwendet werden sollen. Fügen Sie die folgende Anweisung in die RC-Datei ein:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*
</dt> <dd>

Numerischer Ausdruck, der den Bezeichner angibt, mit dem das Menü während der [**WM- \_ Hilfe**](../shell/wm-help.md) Verarbeitung identifiziert wird

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupbody*
</dt> <dd>

Enthält eine beliebige Kombination der [**MenuItem**](menuitem-statement.md) -und [**Popup**](popup-resource.md) -Anweisungen.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

Die gültigen arithmetischen und booleschen Vorgänge, die in einem der numerischen Ausdrücke in den Anweisungen von **menuex** enthalten sein können, lauten wie folgt:

-   Hinzufügen ("+")
-   Subtraktion ("-")
-   Unäres Minuszeichen ("-")
-   Unärer Not (' ~ ')
-   Und (' & ')
-   Oder (' \| ')

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Menüs](./using-menus.md)
</dt> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Dialog**](dialog-resource.md)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**Up**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 
