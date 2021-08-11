---
title: DIALOGEX-Ressource
description: Definiert ein Dialogfeld. | DIALOGEX-Ressource
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- DIALOGEX-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e999d4f42477451fef25bd59fb95606624cc4fd60d340231b3ee95558834d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235309"
---
# <a name="dialogex-resource"></a>DIALOGEX-Ressource

Definiert ein Dialogfeld. Die -Anweisung definiert die Position und Die Abmessungen des Dialogfelds auf dem Bildschirm sowie den Stil des Dialogfelds. Außerdem wird Folgendes definiert:

-   Hilfe-IDs im Dialogfeld selbst sowie in Steuerelementen innerhalb des Dialogfelds.
-   Verwendung der [**EXSTYLE-Anweisung**](exstyle-statement.md) für das Dialogfeld selbst sowie für Steuerelemente innerhalb des Dialogfelds.
-   Schriftbreite und italische Einstellungen für die Schriftart, die im Dialogfeld verwendet werden soll.
-   Steuerelementspezifische Daten für Steuerelemente im Dialogfeld.
-   Verwendung der vordefinierten Systemklassennamen **BEDIT,** **IEDIT** und **HEDIT.**

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Eindeutiger Name oder ein eindeutiger 16-Bit-Ganzzahlwert ohne Vorzeichen, der das Dialogfeld identifiziert.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Position auf dem Bildschirm auf der linken Seite des Dialogfelds in Dialogeinheiten.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Position auf dem Bildschirm am oberen Rand des Dialogfelds in Dialogeinheiten.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Breite*
</dt> <dd>

Breite des Dialogfelds in Dialogeinheiten.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Höhe*
</dt> <dd>

Höhe des Dialogfelds in Dialogeinheiten.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Numerischer Ausdruck, der die ID angibt, mit der das Dialogfeld während der [**WM \_ HELP-Verarbeitung**](../shell/wm-help.md) identifiziert wird.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale -Anweisungen*
</dt> <dd>

Optionen für das Dialogfeld. Dies kann null oder mehr der folgenden Anweisungen sein.



| -Anweisung.                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CAPTION** "*text*"                                              | Beschriftung des Dialogfelds, wenn es über eine Titelleiste verfügt. Weitere Informationen finden Sie unter [**CAPTION-Anweisung.**](caption-statement.md)                                                                                                                                                                                                                                                                                                                                                            |
| **CHARACTERISTICS** *dword*                                       | Benutzerdefinierter **DWORD-Wert** zur Verwendung durch Ressourcentools. Dieser Wert wird vom System nicht verwendet. Weitere Informationen finden Sie unter [**CHARACTERISTICS-Anweisung.**](characteristics-statement.md)                                                                                                                                                                                                                                                                                               |
| **CLASS-Klasse**                                                  | Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelte Anführungszeichen () eingeschlossen ist und die Klasse des Dialogfelds identifiziert. Weitere Informationen finden Sie unter [**CLASS-Anweisung.**](class-statement.md)                                                                                                                                                                                                                                                                                     |
| **EXSTYLE** =  *Erweiterte Stile*                                    | Erweiterter Fensterstil des Dialogfelds. Weitere Informationen finden Sie unter [**EXSTYLE-Anweisung.**](exstyle-statement.md)                                                                                                                                                                                                                                                                                                                                                                    |
| **FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset* | Punktgröße und Schriftart für die Schriftart. Verwenden Sie für *die Gewichtung* die in WinGDI.h definierten *\_ \* *FW_-Werte.* Geben Sie für _italic* TRUE an, um eine italische Schriftart zu verwenden, andernfalls FALSE. Verwenden Sie für *charset* den Wert, der im **lfCharSet-Member** der [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) definiert ist. Um die endgültige Schriftart für ein Dialogfeld abzurufen, sollte eine Anwendung *charset* zusammen mit anderen Schriftarteigenschaften angeben. Weitere Informationen finden Sie unter [**FONT-Anweisung.**](font-statement.md) |
| **LANGUAGE** *language*, *sublanguage*                            | Sprache des Dialogfelds. Weitere Informationen finden Sie unter [**LANGUAGE-Anweisung.**](language-statement.md)                                                                                                                                                                                                                                                                                                                                                                               |
| **MENU menuname**                                                | Zu verwendende Menü. Dieser Wert ist entweder der Name des Menüs oder sein ganzzahliger Bezeichner. Weitere Informationen finden Sie unter [**MENU-Anweisung.**](menu-statement.md)                                                                                                                                                                                                                                                                                                                             |
| **STYLE-Stile**                                                 | Stile des Dialogfelds. Weitere Informationen finden Sie unter [**STYLE-Anweisung.**](style-statement.md)                                                                                                                                                                                                                                                                                                                                                                                       |
| **VERSION** *dword*                                               | Benutzerdefinierter **DWORD-Wert.** Diese Anweisung ist für die Verwendung durch zusätzliche Ressourcentools vorgesehen und wird nicht vom System verwendet. Weitere Informationen finden Sie unter [**VERSION-Anweisung.**](version-statement.md)                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*
</dt> <dd>

Der Text der **DIALOGEX-Ressource** besteht aus einer beliebigen Anzahl von Steueranweisungen. Es gibt vier Familien von Steuerelementanweisungen: generisch, statisch, Schaltfläche und Bearbeiten. Weitere Informationen finden Sie in den Hinweisen.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="remarks"></a>Hinweise

Die gültigen Vorgänge, die in einem der numerischen Ausdrücke in den Anweisungen von **DIALOGEX** enthalten sein können, sind wie folgt:

-   Hinzufügen ('+')
-   Subtrahieren ('-')
-   Unäres Minus ('-')
-   Unärer NOT ('~')
-   AND ('&')
-   OR (' \| ')

Der Text der Ressource besteht aus generischen, statischen, Schaltflächen- und Bearbeitungssteuerelementanweisungen. Während jede dieser Anweisungsfamilien eine andere Syntax zum Definieren bestimmter Features ihrer Steuerelemente verwendet, verwenden sie alle eine gemeinsame Syntax zum Definieren von Position, Größe, erweiterten Stilen, Hilfe-ID und steuerelementspezifischen Daten. Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

### <a name="generic-control-statements"></a>Generische Steuerelementanweisungen

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Fenstertext für das Steuerelement. Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*Classname*
</dt> <dd>

Name der Klasse. Dies kann entweder eine Zeichenfolge sein, die in doppelte Anführungszeichen (") eingeschlossen ist, oder eine der folgenden vordefinierten Systemklassen: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR** oder **COMBOBOX**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Fensterstile **(explizite WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* ES \_ \* *_, _* LBS \_ \* *_, _* SBS \_ \* *_, und _* CBS-Stilwerte, \_ \*** die in Winuser.H definiert sind, können verwendet werden, indem der RC-Datei ein Include hinzugefügt wird: `#include "winuser.h"` ). Weitere Informationen finden Sie unter [Fensterstile.](/windows/desktop/winmsg/window-styles)

</dd> </dl>

### <a name="static-control-statements"></a>Statische Steuerungsanweisungen

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT,** **RTEXT** oder **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Fenstertext für das Steuerelement. Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> </dl>

### <a name="button-control-statements"></a>Schaltflächen-Steuerelementanweisungen

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3** oder **USERBUTTON**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Fenstertext für das Steuerelement. Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> </dl>

### <a name="edit-control-statements"></a>Bearbeiten von Steuerelementanweisungen

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT,** **BEDIT,** **HEDIT** oder **IEDIT**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Steuerelement Weitere Informationen finden Sie unter [Allgemeine Steuerungsparameter.](common-control-parameters.md)

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Dialogfeldern](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**Beschleuniger**](accelerators-resource.md)
</dt> <dt>

[**Merkmale**](characteristics-statement.md)
</dt> <dt>

[**Steuerung**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**Sprache**](language-statement.md)
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[Menü](menu-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 
