---
title: DIALOGEX-Ressource
description: Definiert ein Dialogfeld. | DIALOGEX-Ressource
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- DIALOGEX-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219310"
---
# <a name="dialogex-resource"></a>DIALOGEX-Ressource

Definiert ein Dialogfeld. Die-Anweisung definiert die Position und die Dimensionen des Dialog Felds auf dem Bildschirm sowie den Dialogfeld Stil. Außerdem wird Folgendes definiert:

-   Hilfe-IDs im Dialogfeld selbst sowie für Steuerelemente im Dialogfeld.
-   Verwendung der [**ExStyle**](exstyle-statement.md) -Anweisung für das Dialogfeld selbst und für Steuerelemente im Dialogfeld.
-   Schrift Breite und kursiv Einstellungen für die Schriftart, die im Dialogfeld verwendet werden soll.
-   Steuerelement spezifische Daten für Steuerelemente im Dialogfeld.
-   Verwendung der vordefinierten System Klassennamen " **BEDIT**", " **Iedit**" und " **HEdit** ".

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein eindeutiger ganzzahliger 16-Bit-Wert ohne Vorzeichen, der das Dialogfeld identifiziert.

</dd> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Speicherort auf dem Bildschirm der linken Seite des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Speicherort auf dem Bildschirm des oberen Rands des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Breite*
</dt> <dd>

Breite des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Flugh*
</dt> <dd>

Höhe des Dialog Felds in Dialogfeld Einheiten.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*
</dt> <dd>

Numerischer Ausdruck, der die ID angibt, mit der das Dialogfeld während der [**WM- \_ Hilfe**](../shell/wm-help.md) Verarbeitung identifiziert wird.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*
</dt> <dd>

Optionen für das Dialogfeld. Dies kann NULL oder mehr der folgenden-Anweisungen sein.



| -Anweisung.                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Beschriftung** "*Text*"                                              | Beschriftung des Dialog Felds, wenn es über eine Titelleiste verfügt. Weitere Informationen finden Sie unter [**Caption-Anweisung**](caption-statement.md).                                                                                                                                                                                                                                                                                                                                                            |
| **Merkmale** *DWORD*                                       | Benutzerdefinierter **DWORD** -Wert, der von Ressourcen Tools verwendet werden soll. Dieser Wert wird vom System nicht verwendet. Weitere Informationen finden Sie unter [**Characteristics-Anweisung**](characteristics-statement.md).                                                                                                                                                                                                                                                                                               |
| **Class**-_Klasse_                                                  | Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die die Klasse des Dialog Felds angibt. Weitere Informationen finden Sie unter [**Class-Anweisung**](class-statement.md).                                                                                                                                                                                                                                                                                     |
| **ExStyle** =  *Erweiterte Stile*                                    | Erweiterte Fenster Stil des Dialog Felds. Weitere Informationen finden Sie unter [**ExStyle-Anweisung**](exstyle-statement.md).                                                                                                                                                                                                                                                                                                                                                                    |
| **Schriftart** *pointsize*, Schriftart, *Weight*, *kursiv*, *CharSet* | Die Punktgröße und Schriftart für die Schriftart. Verwenden Sie für *Weight* die in WinGDI. h definierten **FW \_ \** _-Werte. Geben Sie für _italic * true an, um eine kursiv Schrift zu verwenden, andernfalls false. Verwenden Sie für *CharSet* den Wert, der im **lfCharSet** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur definiert ist. Um die definitive Schriftart für ein Dialogfeld zu erhalten, sollte eine Anwendung *CharSet* zusammen mit anderen Schriftart Eigenschaften angeben. Weitere Informationen finden Sie unter [**Font-Anweisung**](font-statement.md). |
| **Sprach** *Sprache*, *unter Sprache*                            | Sprache des Dialog Felds. Weitere Informationen finden Sie unter [**Language Statement**](language-statement.md).                                                                                                                                                                                                                                                                                                                                                                               |
|  *MENUNAME darf* -Menü                                               | Das zu verwendende Menü. Dieser Wert ist entweder der Name des Menüs oder der ganzzahlige Bezeichner. Weitere Informationen finden Sie unter [**Menu-Anweisung**](menu-statement.md).                                                                                                                                                                                                                                                                                                                             |
| **Stil** *Stile*                                                | Stile des Dialog Felds. Weitere Informationen finden Sie unter [**Style-Anweisung**](style-statement.md).                                                                                                                                                                                                                                                                                                                                                                                       |
| **Version** *DWORD*                                               | Benutzerdefinierter **DWORD** -Wert. Diese Anweisung ist für die Verwendung durch zusätzliche Ressourcen Tools vorgesehen und wird nicht vom System verwendet. Weitere Informationen finden Sie unter [**Versions Anweisung**](version-statement.md).                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*Control-Anweisungen*
</dt> <dd>

Der Text der **DIALOGEX** -Ressource besteht aus einer beliebigen Anzahl von Steuerungs Anweisungen. Es gibt vier Familien von Steuerungs Anweisungen: generisch, statisch, Schaltfläche und bearbeiten. Weitere Informationen finden Sie in den Hinweisen.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="remarks"></a>Bemerkungen

Die gültigen Vorgänge, die in einem der numerischen Ausdrücke in den Anweisungen von **DIALOGEX** enthalten sein können, lauten wie folgt:

-   Hinzufügen ("+")
-   Subtraktion ("-")
-   Unäres Minuszeichen ("-")
-   Unärer Not (' ~ ')
-   Und (' & ')
-   Oder (' \| ')

Der Hauptteil der Ressource besteht aus generischen, statischen, Schaltflächen-und Bearbeitungs Steuerungs Anweisungen. Obwohl jede dieser Aufstellungen eine andere Syntax zum Definieren spezifischer Features Ihrer Steuerelemente verwendet, haben Sie alle eine gemeinsame Syntax zum Definieren von Position, Größe, erweiterten Stilen, Hilfe Identifikationsnummer und Steuerungs spezifischen Daten. Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

### <a name="generic-control-statements"></a>Generische Steuerungs Anweisungen

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*ControlText*
</dt> <dd>

Fenster Text für das Steuerelement. Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*ClassName*
</dt> <dd>

Name der Klasse. Dabei kann es sich um eine Zeichenfolge handeln, die in doppelten Anführungszeichen (") oder einer der folgenden vordefinierten System Klassen eingeschlossen ist: **Schaltfläche**, **statisch**, **Bearbeiten**, **ListBox**, **Scrollleiste** oder **ComboBox**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Fenster Stile (explizite, in winuser. H definierte Werte von **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ und _* CBS \_ \*** können verwendet werden, indem der RC-Datei eine include-Datei hinzugefügt `#include "winuser.h"` wird: Weitere Informationen finden Sie unter [Fenster Stile](/windows/desktop/winmsg/window-styles).

</dd> </dl>

### <a name="static-control-statements"></a>Statische Steuerelement Anweisungen

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticclass*
</dt> <dd>

**LTEXT**, **rtext** oder **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*ControlText*
</dt> <dd>

Fenster Text für das Steuerelement. Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> </dl>

### <a name="button-control-statements"></a>Button-Steuerelement Anweisungen

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*ButtonClass*
</dt> <dd>

**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CheckBox**, **PUSHBOX**, **PUSHBUTTON**, **RadioButton**, **STATE3** oder **userButton**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*ControlText*
</dt> <dd>

Fenster Text für das Steuerelement. Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> </dl>

### <a name="edit-control-statements"></a>Edit Control-Anweisungen

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*EditClass*
</dt> <dd>

**EDITTEXT**, **BEDIT**, **HEdit** oder **Iedit**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Dialog Feldern](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**Accelerators**](accelerators-resource.md)
</dt> <dt>

[**Charakteristik**](characteristics-statement.md)
</dt> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[**"Kreatedialog"**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**Kurse**](language-statement.md)
</dt> <dt>

[**"LogFont"**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[Stehen](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 
