---
title: ARIA-Bezeichnungsfehler
description: ARIA-Bezeichnungsfehler
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42abee9028db8c3a4070d9b60d0650187339fc4c9ec34d0b70f720c27e973897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122320"
---
# <a name="aria-label-error"></a>ARIA-Bezeichnungsfehler

## <a name="text"></a>Text

Das Element hat den Typ **Eingabe,** **Schaltfläche,** **Bildschaltfläche** oder Orientierungspunkt,  hat aber keinen barrierefreien Namen.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für:

-   Formulareingabefelder:
    -   HTML-Tags– Eingabetyp= "Textkennwort-Kontrollkästchen Optionsdatei **\[ \| \| \| \| \| \| \| E-Mail tel color \| \| datetime \| datetime-local \| time \| \| \| \| \| \| \]** week month range search url" **,** wählen Sie , **datalist** und **textarea** aus.
    -   TS-ARIA-Rollen:Kontrollkästchen, Kombinationsfeld, Listenfeld, Optionsfeld, Optionsfeld, **Textfeld,** **Struktur,** **Schieberegler** und **Spinbutton**. 
-   Bilder/Bildschaltflächen/Schaltflächen
    -   HTML-Tags–**img**, **input \[ type="image \| button" \]** und **button**.
    -   TS-ARIA-Rollen–**img** und **schaltfläche**.
-   Besondere Merkmale
    -   TS-ARIA-Rollen–**Region**, **Banner**, **ergänzende**, **Inhaltsinfo**, **Form**, **Haupt-**, **Navigations-** und **Suche**.

> [!Note]  
> AccChecker zeigt diesen Fehler auch für Elemente an, für die der barrierefreie Name standardmäßig basierend auf innerem HTML-Inhalt festgelegt ist (siehe banner-Element im obigen Beispiel).  In diesen Fällen können Sie diese Fehler unterdrücken.

 

Alle semantisch wichtigen Benutzeroberflächenelemente wie Formularfelder (z. B. **Eingabe,** Auswahl **,** **Textbereich),** Bilder, Schaltflächen und Sehenswürdigkeiten (Tags, die logische Bereiche darstellen) müssen über den barrierefreien Namen verfügen, damit Spracheingaben sie ordnungsgemäß ankündigen können.

Um diesen Fehler zu beheben, legen Sie den barrierefreien Namen auf eine der folgenden Arten fest (in der Reihenfolge der Bevorzugten aufgeführt).

-   Formularfelder: Verwenden Sie das **Bezeichnungstag,** und legen Sie **das for-Attribut** auf den **ID-Wert** des Zielfelds fest.
-   Bild-/Bildschaltfläche: Legen Sie das **attribut alt** fest.
-   Schaltflächen: Legen Sie den Text der Schaltflächenbeschriftung fest.
-   Für jedes Element:
    -   [**Attribut "aria-und-labelby":**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) Wird auf den **ID-Wert** des Elements festgelegt, das die Zeichenfolge für den barrierefreien Namen enthält.
    -   [**aria-label-Attribut:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) Legen Sie auf die barrierefreie Namenszeichenfolge fest.
    -   [**title-Attribut:**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) Legen Sie auf die barrierefreie Namenszeichenfolge fest (erstellen Sie auch eine **QuickInfo).**

## <a name="example"></a>Beispiel


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




