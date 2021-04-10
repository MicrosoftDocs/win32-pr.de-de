---
title: Anhang E Text Attribute für Active Accessibility Text Dienste-Wörterbuch
description: Dieser Anhang enthält Informationen zu Textattributen, die in iaccdictionary definiert sind.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588c827764d17c2576efaa5e3117527e23d1da26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039554"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Anhang E: Text Attribute für Active Accessibility Text Dienste-Wörterbuch

Dieser Anhang enthält Informationen zu Textattributen, die in [**iaccdictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)definiert sind. Es ist als eine Reihe von Tabellen organisiert. Jede Tabelle enthält Informationen zu einer bestimmten Kategorie von Attributen. Diese Kategorien sind tatsächlich gescht, sind aber unten getrennt, sodass Sie die Attribute sehen können.

> [!Note]  
> Active Accessibility Text Dienste sind veraltet. Weitere Informationen zu erweiterten Text Eingaben und Technologien für natürliche Sprache finden Sie im [Microsoft Windows-Text Dienst-Framework](../tsf/text-services-framework.md) .

 

Jeder Eintrag in einer Tabelle enthält einen Attributnamen und anzeigen Amen, einen Typ, Cascading Stylesheets (CSS) äquivalent, ein entsprechendes Text Objektmodell (Tom) und ggf. weitere Kommentare. Die entsprechende Tom-Spalte enthält Informationen über die Tom-Methode, die mit dem-Attribut verwendet wird (Teil der Schnittstellen [**itextfont**](/windows/desktop/api/tom/nn-tom-itextfont), [**itextrange**](/windows/desktop/api/tom/nn-tom-itextrange)oder [**itextpara**](/windows/desktop/api/tom/nn-tom-itextpara) ). Die Informationen vor jeder Tabelle gibt an, welche Schnittstelle die Attribute unterstützt. die Informationen in der entsprechenden Tom-Tabelle gibt den Namen der Methode an. Jeder Eintrag in der Spalte "Tom äquivalente" ist zwei Methoden zugeordnet. Der Namenseintrag ist beispielsweise mit den Methoden **GetName** und **SetName** verknüpft.

Weitere Informationen zu diesen Schnittstellen finden Sie in der Dokumentation zum [Text Objektmodell](../controls/text-object-model.md) im Windows Software Development Kit (SDK).

## <a name="font"></a>Schriftart

Die Attribute in der folgenden Tabelle sind allgemeinen Schriftart Attributen zugeordnet. Die Tom-Entsprechung ist die [**itextfont**](/windows/desktop/api/tom/nn-tom-itextfont) -Schnittstelle.



| Attribut Name, Anzeige Name       | type     | CSS-Entsprechung       | Tom-Entsprechung | Kommentar           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Font- \_ fakename, fakename<br/> | VT \_ BSTR | Font-Family: Verdana | Name           |                   |
| Schriftart- \_ sizepts, sizepts<br/>   | VT \_ I4   | Font-size: XPT       | Size           | Größe ist in Punkten |



 

## <a name="font_style"></a>Schriftart \_ Stil

Die Attribute in der folgenden Tabelle berücksichtigen Schriftart Format Attribute (z. b., ob der Text fett oder kursiv festgelegt ist). Die Tom-Entsprechung ist die [**itextfont**](/windows/desktop/api/tom/nn-tom-itextfont) -Schnittstelle.



| Attribut Name, Anzeige Name                             | type     | CSS-Entsprechung              | Tom-Entsprechung                                            | Kommentar                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Schriftart \_ fett formatiert \_ , fett formatiert<br/>                        | VT \_ bool | Schriftart-Gewichtung: Fett           | Fett                                                      |                           |
| Schrift \_ Schnitt \_ kursiv kursiv, kursiv<br/>                    | VT \_ bool | Schriftart Stil: kursiv          | Kursiv                                                    |                           |
| SmallCaps im Schrift Schnitt \_ \_ , SmallCaps<br/>              | VT \_ bool | Schriftart-Variant: Small-Caps    | Kapitälchen                                                 |                           |
| Schrift Schnitt groß geschrieben \_ \_ , Großbuchstaben<br/>             | VT \_ bool | Text-Transform: Großbuchstaben  | Nicht unterstützt                                             |                           |
| Schriftart \_ Stil \_ Großbuchstaben, Großbuchstaben<br/>               | VT \_ bool | Text-Transform: Großbuchstaben   | Großbuchstaben                                                   |                           |
| Schriftart \_ Stil \_ Kleinbuchstaben, Kleinbuchstaben<br/>               | VT \_ bool | Text-Transform: Kleinbuchstaben   | Nicht unterstützt                                             |                           |
| \_Schriftstil \_ Prägung, Prägung<br/>                     | VT \_ bool | Nicht unterstützt               | Emboss                                                    |                           |
| Schrift \_ Schnitt \_ , engrab<br/>                   | VT \_ bool | Nicht unterstützt               | Umschließen                                                   |                           |
| Schriftart \_ Stil \_ ausgeblendet                                       | VT \_ bool | Nicht unterstützt               | Ausgeblendet                                                    |                           |
| Schriftart \_ Stil \_ : Kerning, Kerning<br/>                   | VT \_ R4   | Nicht unterstützt               | Unterschneidungen                                                   | Dieselben Werte wie getkerning |
| Stil der Schriftart \_ \_ , beschrieben<br/>                 | VT \_ bool | Nicht unterstützt               | Umriss                                                  |                           |
| Schriftart \_ \_ , Position, Position<br/>                 | VT \_ R4   | Nicht unterstützt               | Position                                                  |                           |
| Schriftart \_ Stil \_ geschützt                                    | VT \_ bool | Nicht unterstützt               | Protected                                                 |                           |
| Schrift \_ Schnitt \_ Schatten, Schatten<br/>                     | VT \_ bool | Zeilenhöhe (Minuszahlen) | Shadow                                                    |                           |
| Abstand zwischen Schriftart \_ \_ und Abstand<br/>                   | VT \_ R4   | Buchstabe-Abstand              | Abstand                                                   | In Punkten                 |
| Schrift \_ Arten \_ Gewichtung, Gewichtung<br/>                     | VT \_ I4   | Schrift Breite                 | Gewichtsgewichtungs-und getweight-Werte<br/> |                           |
| Schrift \_ Schnitt \_ Höhe, Höhe<br/>                     | VT \_ R4   | line-height                 | Nicht unterstützt                                             | In Punkten                 |
| Schriftart \_ Stil \_ blinken, blinken<br/>                       | VT \_ bool | Text-Dekoration: blinken      | Nicht unterstützt                                             |                           |
| Schrift \_ Schnitt \_ , Index, Index<br/>               | VT \_ bool | Vertikale Ausrichtung: Sub         | Index (auch Position)                                 |                           |
| Schrift \_ Schnitt \_ SuperScript, SuperScript<br/>           | VT \_ bool | Vertikale Ausrichtung: Super       | Superscript (auch Position)                               |                           |
| Schriftart \_ \_ Farbe, Farbe<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | RBG COLORREF-Stil        |
| \_Hintergrundfarbe für Schriftart Stil \_ , Hintergrund \_ Farbe<br/> | VT \_ I4   | Hintergrundfarbe            | BackColor                                                 | RBG COLORREF-Stil        |



 

## <a name="font_style_animation"></a>Animation im Schriftart \_ Stil \_

Die Attribute in der folgenden Tabellen Adress Animation. Die Tom-Entsprechung ist die [**itextfont**](/windows/desktop/api/tom/nn-tom-itextfont) -Schnittstelle.



| Attribut Name, Anzeige Name                                              | type     | CSS-Entsprechung | Tom-Entsprechung |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| Schriftart \_ Stil \_ Animation \_ lasvegaslights, LasVegas- \_ Leuchten<br/>         | VT \_ bool | Nicht unterstützt  | Animation      |
| Animation des Schriftart \_ Stils \_ \_ blinkingbackground, Blinken des \_ Hintergrunds<br/> | VT \_ bool | Nicht unterstützt  | Animation      |
| Animation für Schriftart \_ Stil \_ \_ , sparkletext, Glanz \_ Text<br/>               | VT \_ bool | Nicht unterstützt  | Animation      |
| Schriftart \_ Stil \_ Animation \_ marchingblackants, marschierende \_ schwarze \_ Ameisen<br/> | VT \_ bool | Nicht unterstützt  | Animation      |
| Animation des Schrift \_ Stils \_ \_ marchingredants, marschierende \_ Rote \_ Ameisen<br/>     | VT \_ bool | Nicht unterstützt  | Animation      |
| \_ \_ Animationshimmer für Schriftart Stil \_ , Shimmer<br/>                         | VT \_ bool | Nicht unterstützt  | Animation      |
| \_ \_ Wipindown-Animation für Schriftart Stil \_ , wipindown<br/>                       | VT \_ bool | Nicht unterstützt  | Animation      |
| Schriftart \_ Stil \_ Animation \_ wiperight, wiperight<br/>                     | VT \_ bool | Nicht unterstützt  | Animation      |



 

## <a name="font_style_underline"></a>Unter \_ Streichung des Schrift Stils \_

Die Attribute in der folgenden Tabellen Adresse unterstreichen Stile für Schriftarten. Die Tom-Entsprechung ist die [**itextfont**](/windows/desktop/api/tom/nn-tom-itextfont) -Schnittstelle.



| Attribut Name, Anzeige Name                     | type     | CSS-Entsprechung                | Tom-Entsprechung |
|---------------------------------------------------|----------|-------------------------------|----------------|
| Schriftart \_ Stil \_ \_ : Single, Single<br/>  | VT \_ bool | Text-Dekoration: Unterstreichung    | Underline      |
| Schriftart \_ Stil \_ \_ unterstrichen Double, Double<br/> | VT \_ bool | Text-Dekoration: durch Leitung | Durchgestrichen  |



 

## <a name="font_style_strikethrough"></a>Schriftart \_ Stil \_ durchgestrichen

Die Attribute in der folgenden Tabelle adressieren die Stile für Schriftarten durchgestrichen.



| Attribut Name, Anzeige Name                                         | type     | CSS-Entsprechung | Tom-Entsprechung |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| Schrift \_ Schnitt \_ \_ : einzeln durchgestrichen, \_ durch \_ Einzel Schlag<br/> | VT \_ bool | Nicht unterstützt  | Nicht unterstützt  |
| Schriftart \_ Stil \_ durchgestrichen \_ , Double, Schlag \_ durch \_ Double<br/> | VT \_ bool | Nicht unterstützt  | Nicht unterstützt  |



 

## <a name="font_style_overline"></a>Schriftart für Schriftart \_ Stil \_

Die Attribute in der folgenden Tabelle behandeln Überschriften Stile für Schriftarten.



| Attribut Name, Anzeige Name                             | type     | CSS-Entsprechung            | Tom-Entsprechung |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Schrift \_ Schnitt \_ über line \_ , Single, Overline \_ Single<br/> | VT \_ bool | Text-Dekoration: über Linie | Nicht unterstützt  |
| Schrift \_ Schnitt \_ über Zeile \_ Double, Overline \_ Double<br/> | VT \_ bool | Text-Dekoration: über Linie | Nicht unterstützt  |



 

## <a name="text"></a>Text

Die Attribute in der folgenden Tabelle behandeln allgemeine Text Formatierungs Attribute.



| Attribut Name, Anzeige Name                     | type        | CSS-Entsprechung | Tom-Entsprechung                                       | Kommentar                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| \_Textverticalwriting, vertikales schreiben<br/> | VT \_ bool    | Nicht unterstützt  | Nicht unterstützt                                        | Wie von Chinesisch/Japanisch verwendet                                                           |
| Text \_ RightToLeft, RightToLeft<br/>          | VT \_ bool    | Richtung      | Nicht unterstützt                                        |                                                                                       |
| Text schreibgeschützt, schreibgeschützt \_<br/>               | VT \_ bool    | Nicht unterstützt  | Itextfont:: canchange, itextrange:: CanEdit            | Die bearbeitet-Eigenschaft des Dokuments hat Vorrang.                                     |
| Text \_ Sprache, Sprache<br/>                | VT \_ I4      | Nicht unterstützt  | Itextfont:: getlanguageid, itextfont:: setlanguageid   | LANGID                                                                                |
| Text \_ Ausrichtung, Ausrichtung<br/>          | VT \_ I4      | Nicht unterstützt  | Nicht unterstützt                                        | 10??? eines gewissen Grades                                                                     |
| Text \_ embedtodobject, eingebettetes \_ Objekt<br/>  | VT \_ bool    | Nicht unterstützt  | Nicht unterstützt                                        | Ermöglicht das Suchen nach eingebetteten Objekten                                                 |
| \_Textlink, Link<br/>                        | VT \_ unbekannt | Link           | Nicht unterstützt                                        | Ein Schnittstellen Zeiger auf das-Objekt. QueryInterface für jede beliebige Schnittstelle aufzurufen |
| Text- \_ Bindestriche, Bindestriche<br/>          | VT \_ bool    | Nicht unterstützt  | Itextpara:: gethyphenations, itextpara:: Abschnitt Zeichen |                                                                                       |



 

## <a name="text_alignment"></a>Text \_ Ausrichtung

Die Attribute in der folgenden Tabelle behandeln die Textausrichtung. Die Tom-Entsprechung ist die [**itextpara**](/windows/desktop/api/tom/nn-tom-itextpara) -Schnittstelle.



| Attribut Name, Anzeige Name               | type     | CSS-Entsprechung | Tom-Entsprechung |
|---------------------------------------------|----------|----------------|----------------|
| Text \_ Ausrichtung \_ Links, Links<br/>       | VT \_ bool | Text-align     | Ausrichtung      |
| Text \_ Ausrichtung \_ Rechts, rechts<br/>     | VT \_ bool | Text-align     | Ausrichtung      |
| Text \_ Ausrichtungs \_ zentrieren, zentrieren<br/>   | VT \_ bool | Text-align     | Ausrichtung      |
| Text \_ Ausrichtung \_ rechtfertigen, rechtfertigen<br/> | VT \_ bool | Text-align     | Ausrichtung      |



 

## <a name="text_para"></a>Text- \_ para

Die Attribute in der folgenden Tabelle behandeln die Formatierung für Absätze. Die Tom-Entsprechung ist die [**itextpara**](/windows/desktop/api/tom/nn-tom-itextpara) -Schnittstelle.



| Attribut Name, Anzeige Name                              | type   | CSS-Entsprechung | Tom-Entsprechung  | Kommentar |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Text \_ para \_ FirstLineIndent, erste \_ Zeilen \_ Einzug<br/> | VT \_ R4 | Nicht unterstützt  | Firstlineingedent | In PTS  |
| Text \_ para \_ LeftIndent, Linker \_ Einzug<br/>             | VT \_ R4 | Nicht unterstützt  | Lefteinzug      | In PTS  |
| Text \_ para \_ RightIndent, rechter \_ Einzug<br/>           | VT \_ R4 | Nicht unterstützt  | RightIndent     | In PTS  |
| Text \_ para \_ SpaceAfter, Leerzeichen \_ nach<br/>             | VT \_ R4 | Nicht unterstützt  | Leerraum      | In PTS  |
| Text \_ para \_ SpaceBefore, Leerzeichen \_ nach<br/>            | VT \_ R4 | Nicht unterstützt  | Leerraum      | In PTS  |



 

## <a name="text_para_linespacing"></a>Text- \_ para \_ LineSpacing

Die Attribute in der folgenden Tabelle behandeln den Zeilenabstand in Absätzen. Die Tom-Entsprechung ist die [**itextpara**](/windows/desktop/api/tom/nn-tom-itextpara) -Schnittstelle.



| Attribut Name, Anzeige Name                               | type     | CSS-Entsprechung | Tom-Entsprechung | Kommentar  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Text \_ para \_ linespacung \_ Single, Single<br/>           | VT \_ bool | Nicht unterstützt  | Zeilenabstand    |          |
| Text \_ para \_ \_ linespacingoneptfive, One \_ PT \_ Five<br/> | VT \_ bool | Nicht unterstützt  | Zeilenabstand    |          |
| Text \_ para \_ linespacung \_ Double, Double<br/>           | VT \_ bool | Nicht unterstützt  | Zeilenabstand    |          |
| Text \_ para \_ linespacat mindestens \_ , \_ mindestens<br/>       | VT \_ R4   | Nicht unterstützt  | Zeilenabstand    | In Zeilen |
| Text- \_ para \_ linespacingexakt \_ , genau<br/>         | VT \_ R4   | Nicht unterstützt  | Zeilenabstand    | In Zeilen |
| Text \_ para \_ \_ linespacingmutiple, Multiple<br/>        | VT \_ R4   | Nicht unterstützt  | Zeilenabstand    | In Zeilen |



 

## <a name="text_list"></a>\_Textliste

Die Attribute in der folgenden Tabelle Adresslisten und Ebenen von Text Listen. Die Tom-Entsprechung ist die [**itextpara**](/windows/desktop/api/tom/nn-tom-itextpara) -Schnittstelle.



| Attribut Name, Anzeige Name | type   | CSS-Entsprechung | Tom-Entsprechung | Kommentar                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| \_Textliste \_ levelindex,       | VT \_ I4 | Nicht unterstützt  | Listlevelindex | 1 steht für die äußerste Liste, 2 für die nächste Ebene usw. |



 

## <a name="text_list_type"></a>Text \_ \_ Auflistungstyp

Die Attribute in der folgenden Tabelle Adresslisten Stile für Text. Die Tom-Entsprechung ist die [**itextpara**](/windows/desktop/api/tom/nn-tom-itextpara) -Schnittstelle.



| Attribut Name, Anzeige Name                          | type     | CSS-Entsprechung  | Tom-Entsprechung |
|--------------------------------------------------------|----------|-----------------|----------------|
| Text \_ \_ Auflistungstyp, Aufzählungs Zeichen \_<br/>             | VT \_ bool | List-Type       | ListType       |
| Text \_ \_ Listentyp \_ Arabisch, Arabisch<br/>             | VT \_ bool | List-Style-Type | ListType       |
| Text \_ List \_ Type \_ lowerletter, Lower \_ Letter<br/> | VT \_ bool | List-Style-Type | ListType       |
| Text \_ \_ Auflistungstyp \_ Großbuchstabe, oberer \_ Buchstabe<br/> | VT \_ bool | List-Style-Type | ListType       |
| Text \_ \_ Auflistungstyp \_ LowerRoman, niedrigerer \_ Roman<br/>   | VT \_ bool | List-Style-Type | ListType       |
| \_Textliste \_ Typ \_ UpperRoman, Upper \_ Roman<br/>   | VT \_ bool | List-Style-Type | ListType       |



 

## <a name="app"></a>App



| Attribut Name, Anzeige Name                         | type     | CSS-Entsprechung | Tom-Entsprechung |
|-------------------------------------------------------|----------|----------------|----------------|
| \_Inkorrigier Ende APP, falsche \_ Schreibweise<br/> | VT \_ bool |                | Nicht unterstützt  |
| \_Incorrectgrammar der APP, falsche \_ Grammatik<br/>   | VT \_ bool |                | Nicht unterstützt  |



 

 

