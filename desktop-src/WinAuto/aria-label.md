---
title: Aria-Bezeichnungs Fehler
description: Aria-Bezeichnungs Fehler
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- Arialabelerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039776"
---
# <a name="aria-label-error"></a>Aria-Bezeichnungs Fehler

## <a name="text"></a>Text

Das Element ist vom Typ " **Input**", " **Button**", " **Image** " oder " **Landmark** ", hat aber keinen zugänglichen Namen.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für:

-   Formulareingabe Felder:
    -   HTML-Tags **– \[ Eingabetyp = " \| textkennwort-Kontrollkästchen Optionsfeld- \| \| \| \| e-Mail-Adresse e-Mail-Adresse für \| \| \| \| DateTime \| -Ortszeit-local \| time \| Week \| Month \| Number \| Range \| Search \| \] URL"**, **Select**, **DataList** und **Textarea**.
    -   WAI-ARIA-Rollen –**CheckBox**, **ComboBox**, **ListBox**, **Radio Group**, **Radio**, **Textfeld**, **Tree**, **Slider** und **SpinButton**.
-   Bilder/Bild-Schaltflächen/-Schaltflächen
    -   HTML-Tags –**IMG**, **input \[ Type = "Bild Schaltfläche \| " \]** und **Schaltfläche**.
    -   Rollen "WAI-ARIA" –**IMG** und **Button**.
-   Besondere Merkmale
    -   WAI-ARIA-Rollen –**Region**, **Banner**, **Ergänzung**, **ContentInfo**, **Formular**, **Main**, **Navigation** und **Suche**.

> [!Note]  
> Die Zugriffs Prüfung zeigt diesen Fehler auch für Elemente an, für die der barrierefreie Name standardmäßig auf der Grundlage des inneren HTML-Inhalts festgelegt wird (siehe das **Banner** Element im obigen Beispiel). In diesen Fällen können Sie diese Fehler unterdrücken.

 

Alle semantisch wichtigen Benutzeroberflächen Elemente, wie z. b. Formularfelder (z. b. **Eingabe**, **Select**, **Textarea**), Bilder, Schaltflächen und Markierungen (Tags, die logische Bereiche darstellen) müssen über den zugreif baren Namen verfügen, damit Bildschirm Sprachausgaben diese korrekt ankündigen können.

Um diesen Fehler zu beheben, legen Sie den barrierefreien Namen auf eine der folgenden Weisen fest (in der Reihenfolge der bevorzugte Reihenfolge).

-   Formularfelder: Verwenden Sie das Tag **Bezeichnung** , und legen Sie für das Attribut **für** den **ID** -Wert des Zielfelds fest.
-   Bild/Bild-Schaltfläche: Legen Sie das **alt** -Attribut fest.
-   Buttons: Legen Sie den Text der Schaltflächen Beschriftung fest.
-   Für ein beliebiges Element:
    -   [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribut: wird auf den **ID** -Wert des Elements festgelegt, das die barrierefreie namens Zeichenfolge enthält.
    -   [**Aria-Label-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) Attribut: auf die barrierefreie namens Zeichenfolge festgelegt.
    -   [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) -Attribut: auf die barrierefreie namens Zeichenfolge festgelegt (außerdem **wird eine** QuickInfo erstellt).

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



 

 




