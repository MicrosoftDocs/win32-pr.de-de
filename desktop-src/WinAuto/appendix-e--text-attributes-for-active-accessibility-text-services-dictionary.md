---
title: Anhang E Textattribute für Active Accessibility Text Services-Wörterbuch
description: Dieser Anhang enthält Informationen zu Textattributen, die in IAccDictionary definiert sind.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539583f05e5140d96594490b0038b1a629f7760b13e4de223f6a8a3304c3901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134063"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Anhang E: Textattribute für Active Accessibility Text Services-Wörterbuch

Dieser Anhang enthält Informationen zu Textattributen, die in [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)definiert sind. Sie ist als eine Reihe von Tabellen organisiert. Jede Tabelle enthält Informationen zu einer bestimmten Kategorie von Attributen. Diese Kategorien sind tatsächlich geschachtelt, aber unten getrennt, sodass Sie die Attribute sehen können.

> [!Note]  
> Active Accessibility Text services ist veraltet. Weitere Informationen zu erweiterten Texteingaben und Technologien für natürliche Sprache finden Sie unter [Microsoft Windows Textdienstframework.](../tsf/text-services-framework.md)

 

Jeder Eintrag in einer Tabelle stellt einen Attributnamen und Anzeigenamen, einen Typ, Cascading Stylesheets (CSS)-Entsprechung, eine TOM-Entsprechung (Text Object Model) und ggf. zusätzliche Kommentare bereit. Die entsprechende TOM-Spalte enthält Informationen über die TOM-Methode, die mit dem -Attribut (Teil der [**Schnittstellen ITextFont,**](/windows/desktop/api/tom/nn-tom-itextfont) [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)oder [**ITextPara)**](/windows/desktop/api/tom/nn-tom-itextpara) verwendet wird. Die Informationen vor jeder Tabelle geben an, welche Schnittstelle die Attribute unterstützt. die Informationen in der TOM-äquivalenten Tabelle geben den Namen der Methode an. Jeder Eintrag in der TOM-äquivalenten Spalte ist zwei Methoden zugeordnet. Beispielsweise ist der Name-Eintrag den **Methoden GetName** und **SetName** zugeordnet.

Weitere Informationen zu diesen Schnittstellen finden Sie in der Dokumentation [zum Textobjektmodell](../controls/text-object-model.md) im Windows Software Development Kit (SDK).

## <a name="font"></a>Schriftart

Die Attribute in der folgenden Tabelle sind allgemeinen Schriftartattributen zugeordnet. Die TOM-Entsprechung ist die [**ITextFont-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Attributname, Anzeigename       | type     | CSS-Entsprechung       | TOM-Entsprechung | Kommentar           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| \_Schriftart FaceName, facename<br/> | VT \_ BSTR | Schriftfamilie: Verdana | Name           |                   |
| Font \_ SizePts, sizePts<br/>   | VT \_ I4   | Schriftgrad: Xpt       | Size           | Die Größe ist in Punkten |



 

## <a name="font_style"></a>\_Schriftschnitt

Die Attribute in der folgenden Tabelle beziehen sich auf Schriftschnittattribute (z. B. ob der Text fett oder kursiv festgelegt ist). Die TOM-Entsprechung ist die [**ITextFont-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Attributname, Anzeigename                             | type     | CSS-Entsprechung              | TOM-Entsprechung                                            | Kommentar                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Schriftschnitt \_ \_ fett, fett<br/>                        | VT \_ BOOL | Schriftbreite: fett           | Fett                                                      |                           |
| Schriftschnitt \_ \_ italisch, italisch<br/>                    | VT \_ BOOL | Schriftschnitt: italisch          | Kursiv                                                    |                           |
| \_ \_ Schriftschnitt SmallCaps, smallcaps<br/>              | VT \_ BOOL | Font-variant: small-caps    | Kapitälchen                                                 |                           |
| \_ \_ Schriftschnitt Großschreibung,Großschreibung<br/>             | VT \_ BOOL | Texttransformation: Groß-/Großschreibung  | Nicht unterstützt                                             |                           |
| Schriftschnitt \_ \_ Großbuchstaben, Großbuchstaben<br/>               | VT \_ BOOL | Texttransformation: Großbuchstaben   | Großbuchstaben                                                   |                           |
| Schriftschnitt \_ \_ Kleinbuchstaben, Kleinbuchstaben<br/>               | VT \_ BOOL | Texttransformation: Kleinbuchstaben   | Nicht unterstützt                                             |                           |
| \_ \_ Schriftschnitt- Emboss, emboss<br/>                     | VT \_ BOOL | Nicht unterstützt               | Emboss                                                    |                           |
| Schriftschnitt \_ \_ : 1600000000000<br/>                   | VT \_ BOOL | Nicht unterstützt               | Gravieren                                                   |                           |
| Schriftschnitt \_ \_ ausgeblendet                                       | VT \_ BOOL | Nicht unterstützt               | Ausgeblendet                                                    |                           |
| Kerning \_ im \_ Schriftschnitt, Kerning<br/>                   | VT \_ R4   | Nicht unterstützt               | Kerning                                                   | Gleiche Werte wie GetKerning |
| Gliederung des \_ Schriftschnitts, \_ umranden<br/>                 | VT \_ BOOL | Nicht unterstützt               | Gliederung                                                  |                           |
| \_ \_ Schriftschnittposition, Position<br/>                 | VT \_ R4   | Nicht unterstützt               | Position                                                  |                           |
| Geschützter \_ Schriftschnitt \_                                    | VT \_ BOOL | Nicht unterstützt               | Protected                                                 |                           |
| \_ \_ Schriftschnittschatten, Schatten<br/>                     | VT \_ BOOL | Zeilenhöhe (minus Zahlen) | Shadow                                                    |                           |
| \_ \_ Schriftschnittabstand,Abstand<br/>                   | VT \_ R4   | Buchstabenabstand              | Abstand                                                   | In Punkten                 |
| \_ \_ Schriftschnittgewichtung, Gewichtung<br/>                     | VT \_ I4   | Schriftgrad                 | WeightSame-Werte als Schriftgrad und GetWeight<br/> |                           |
| \_ \_ Schriftschnitthöhe, Höhe<br/>                     | VT \_ R4   | line-height                 | Nicht unterstützt                                             | In Punkten                 |
| Schriftschnitt \_ \_ Blink,blink<br/>                       | VT \_ BOOL | Textdekoration: blink      | Nicht unterstützt                                             |                           |
| Font \_ Style \_ Subscript,subscript<br/>               | VT \_ BOOL | Vertikale Ausrichtung: sub         | Subscript (auch Position)                                 |                           |
| \_ \_ Schriftschnitt– Hochgestellt, hochgestellt<br/>           | VT \_ BOOL | Vertikale Ausrichtung: super       | Hochgestellt (auch Position)                               |                           |
| \_ \_ Schriftschnittfarbe, Farbe<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | RBG-COLORREF-Stil        |
| Font \_ Style \_ BackgroundColor,background \_ color<br/> | VT \_ I4   | Hintergrundfarbe            | Backcolor                                                 | RBG-COLORREF-Stil        |



 

## <a name="font_style_animation"></a>\_ \_ Schriftartstilanimation

Die Attribute in der folgenden Tabelle adressieren die Schriftartanimation. Das TOM-Äquivalent ist die [**ITextFont-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Attributname, Benutzername                                              | type     | CSS-Entsprechung | TOM-Entsprechung |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| \_ \_ Schriftartanimation \_ LasVegasLights,LasVegas lights \_<br/>         | VT \_ BOOL | Nicht unterstützt  | Animation      |
| \_ \_ Schriftartanimation \_ BlinkingBackground,blinkender \_ Hintergrund<br/> | VT \_ BOOL | Nicht unterstützt  | Animation      |
| \_ \_ Schriftartanimation \_ SparkleText,Sparkle-Text \_<br/>               | VT \_ BOOL | Nicht unterstützt  | Animation      |
| Font \_ Style \_ Animation \_ MarchingBlackAnts,marching \_ black \_ ants<br/> | VT \_ BOOL | Nicht unterstützt  | Animation      |
| Font \_ Style \_ Animation \_ MarchingRedAnts,marching \_ red \_ ants<br/>     | VT \_ BOOL | Nicht unterstützt  | Animation      |
| Font \_ Style \_ Animation \_ Shyl, Shyl<br/>                         | VT \_ BOOL | Nicht unterstützt  | Animation      |
| Font \_ Style \_ Animation \_ WipeDown,wipeDown<br/>                       | VT \_ BOOL | Nicht unterstützt  | Animation      |
| \_ \_ Schriftartanimation \_ WipeRight,wipeRight<br/>                     | VT \_ BOOL | Nicht unterstützt  | Animation      |



 

## <a name="font_style_underline"></a>Schriftschnitt \_ \_ unterstrichen

Die Attribute in der folgenden Tabelle adressieren Unterstreichungsstile für Schriftarten. Das TOM-Äquivalent ist die [**ITextFont-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Attributname, Benutzername                     | type     | CSS-Entsprechung                | TOM-Entsprechung |
|---------------------------------------------------|----------|-------------------------------|----------------|
| Schriftschnitt \_ \_ Unterstrichen \_ Single,single<br/>  | VT \_ BOOL | Textdekoration: Unterstrichen    | Underline      |
| Schriftschnitt \_ \_ Unterstrichen \_ Double,double<br/> | VT \_ BOOL | Textdekoration: Durchgestrichen | Durchgestrichen  |



 

## <a name="font_style_strikethrough"></a>\_Durchstreichen des \_ Schriftschnitts

Die Attribute in der folgenden Tabelle adressieren Durchlaufstile für Schriftarten.



| Attributname, Benutzername                                         | type     | CSS-Entsprechung | TOM-Entsprechung |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| Font \_ Style \_ Strikethrough \_ Single,strike \_ through \_ single<br/> | VT \_ BOOL | Nicht unterstützt  | Nicht unterstützt  |
| \_Durchstreichen \_ des \_ Schriftschnitts "Double", \_ "Durchschlagen durch \_ double"<br/> | VT \_ BOOL | Nicht unterstützt  | Nicht unterstützt  |



 

## <a name="font_style_overline"></a>\_ \_ Schriftschnittüberlinie

Die Attribute in der folgenden Tabelle adressieren Overlinestile für Schriftarten.



| Attributname, Benutzername                             | type     | CSS-Entsprechung            | TOM-Entsprechung |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Font \_ Style \_ Overline \_ Single,overline \_ single<br/> | VT \_ BOOL | Textdekoration: Überlinie | Nicht unterstützt  |
| Schriftschnitt \_ \_ Überlinie \_ Double,Overline double \_<br/> | VT \_ BOOL | Textdekoration: Überlinie | Nicht unterstützt  |



 

## <a name="text"></a>Text

Die Attribute in der folgenden Tabelle adressieren allgemeine Textformatierungsattribute.



| Attributname, Benutzername                     | type        | CSS-Entsprechung | TOM-Entsprechung                                       | Kommentar                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Text \_ VerticalWriting, vertikales Schreiben<br/> | VT \_ BOOL    | Nicht unterstützt  | Nicht unterstützt                                        | Wie von Chinesisch/Japanisch verwendet                                                           |
| Text \_ RightToLeft,righttoleft<br/>          | VT \_ BOOL    | Direction      | Nicht unterstützt                                        |                                                                                       |
| Text \_ ReadOnly, schreibgeschützt<br/>               | VT \_ BOOL    | Nicht unterstützt  | ITextFont::CanChange, ITextRange::CanEdit            | Die bearbeitbare Eigenschaft des Dokuments hat Vorrang.                                     |
| \_Textsprache, Sprache<br/>                | VT \_ I4      | Nicht unterstützt  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | Langid                                                                                |
| \_Textausrichtung,Ausrichtung<br/>          | VT \_ I4      | Nicht unterstützt  | Nicht unterstützt                                        | 10??? eines Grads                                                                     |
| Text \_ EmbeddedObject,eingebettetes \_ Objekt<br/>  | VT \_ BOOL    | Nicht unterstützt  | Nicht unterstützt                                        | Ermöglicht die Suche nach eingebetteten Objekten.                                                 |
| \_Textlink, Link<br/>                        | VT \_ UNKNOWN | Link           | Nicht unterstützt                                        | Ein Schnittstellenzeiger auf das Objekt; Aufrufen von QueryInterface für eine beliebige Schnittstelle von Interesse |
| \_Text-Bindestriche,Bindestriche<br/>          | VT \_ BOOL    | Nicht unterstützt  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>\_Textausrichtung

Die Attribute in der folgenden Tabelle adressiert die Textausrichtung. Das TOM-Äquivalent ist die [**ITextPara-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Attributname, Benutzername               | type     | CSS-Entsprechung | TOM-Entsprechung |
|---------------------------------------------|----------|----------------|----------------|
| \_ \_ Textausrichtung Links,links<br/>       | VT \_ BOOL | Text ausrichten     | Ausrichtung      |
| \_Textausrichtung \_ rechts, rechts<br/>     | VT \_ BOOL | Text ausrichten     | Ausrichtung      |
| \_ \_ Textausrichtungscenter, Mitte<br/>   | VT \_ BOOL | Text ausrichten     | Ausrichtung      |
| \_Textausrichtung, \_ Begründung<br/> | VT \_ BOOL | Text ausrichten     | Ausrichtung      |



 

## <a name="text_para"></a>Text \_ Para

Die Attribute in der folgenden Tabelle enthalten die Adressformatierung für Absätze. Das TOM-Äquivalent ist die [**ITextPara-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Attributname, Benutzername                              | type   | CSS-Entsprechung | TOM-Entsprechung  | Kommentar |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Text \_ Para \_ FirstLineIndent,erster \_ \_ Zeileneinzug<br/> | VT \_ R4 | Nicht unterstützt  | FirstLineIndent | In pts  |
| Text \_ Para \_ LeftIndent,linker \_ Einzug<br/>             | VT \_ R4 | Nicht unterstützt  | LeftIndent      | In pts  |
| Text \_ para \_ RightIndent,right \_ indent<br/>           | VT \_ R4 | Nicht unterstützt  | RightIndent     | In pts  |
| Text \_ Para \_ SpaceAfter,Leerzeichen \_ nach<br/>             | VT \_ R4 | Nicht unterstützt  | SpaceAfter      | In pts  |
| Text \_ Para \_ SpaceBefore,space \_ after<br/>            | VT \_ R4 | Nicht unterstützt  | SpaceAfter      | In pts  |



 

## <a name="text_para_linespacing"></a>Text \_ para \_ lineSpacing

Die Attribute in der folgenden Tabelle adressieren den Zeilenabstand in Absätzen. Die TOM-Entsprechung ist die [**ITextPara-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Attributname, Anzeigename                               | type     | CSS-Entsprechung | TOM-Entsprechung | Kommentar  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Text \_ para \_ lineSpacing \_ Single, single<br/>           | VT \_ BOOL | Nicht unterstützt  | Zeilenabstand    |          |
| Text \_ para \_ lineSpacing \_ OnePtFive,one \_ pt \_ five<br/> | VT \_ BOOL | Nicht unterstützt  | Zeilenabstand    |          |
| Text \_ Para \_ lineSpacing \_ Double,double<br/>           | VT \_ BOOL | Nicht unterstützt  | Zeilenabstand    |          |
| Text \_ para \_ lineSpacing \_ AtLeast,least \_<br/>       | VT \_ R4   | Nicht unterstützt  | Zeilenabstand    | In Zeilen |
| Text \_ Para \_ lineSpacing \_ Exactly,exactly<br/>         | VT \_ R4   | Nicht unterstützt  | Zeilenabstand    | In Zeilen |
| Text \_ Para \_ lineSpacing \_ Mutiple,multiple<br/>        | VT \_ R4   | Nicht unterstützt  | Zeilenabstand    | In Zeilen |



 

## <a name="text_list"></a>\_Textliste

Die Attribute in der folgenden Tabelle adressiert Listen und Ebenen von Textlisten. Die TOM-Entsprechung ist die [**ITextPara-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Attributname, Anzeigename | type   | CSS-Entsprechung | TOM-Entsprechung | Kommentar                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| Text \_ List \_ LevelIndex,       | VT \_ I4 | Nicht unterstützt  | ListLevelIndex | Wobei 1 die äußerste Liste ist, 2 die nächste Ebene usw. |



 

## <a name="text_list_type"></a>\_ \_ Textlistentyp

Die Attribute in der folgenden Tabelle enthalten Adresslistenstile für Text. Die TOM-Entsprechung ist die [**ITextPara-Schnittstelle.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Attributname, Anzeigename                          | type     | CSS-Entsprechung  | TOM-Entsprechung |
|--------------------------------------------------------|----------|-----------------|----------------|
| \_ \_ Textlistentyp \_ Aufzählungszeichen, Aufzählungszeichen<br/>             | VT \_ BOOL | Listentyp       | ListType       |
| \_ \_ Textlistentyp \_ Arabisch, Arabisch<br/>             | VT \_ BOOL | List-style-type | ListType       |
| \_ \_ Textlistentyp \_ LowerLetter,Kleinbuchstabe \_<br/> | VT \_ BOOL | List-style-type | ListType       |
| \_ \_ Textlistentyp \_ UpperLetter, \_ Großbuchstabe<br/> | VT \_ BOOL | List-style-type | ListType       |
| \_ \_ Textlistentyp \_ LowerBuchstaben,lower \_ roman<br/>   | VT \_ BOOL | List-style-type | ListType       |
| \_ \_ Textlistentyp \_ UpperStufe, \_ Oberer Roman<br/>   | VT \_ BOOL | List-style-type | ListType       |



 

## <a name="app"></a>App



| Attributname, Anzeigename                         | type     | CSS-Entsprechung | TOM-Entsprechung |
|-------------------------------------------------------|----------|----------------|----------------|
| App \_ IncorrectSpelling, falsche \_ Schreibweise<br/> | VT \_ BOOL |                | Nicht unterstützt  |
| App \_ IncorrectGrammar, falsche \_ Grammatik<br/>   | VT \_ BOOL |                | Nicht unterstützt  |



 

 

