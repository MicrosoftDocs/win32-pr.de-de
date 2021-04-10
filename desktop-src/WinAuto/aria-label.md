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
# <a name="aria-label-error"></a><span data-ttu-id="17140-104">Aria-Bezeichnungs Fehler</span><span class="sxs-lookup"><span data-stu-id="17140-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="17140-105">Text</span><span class="sxs-lookup"><span data-stu-id="17140-105">Text</span></span>

<span data-ttu-id="17140-106">Das Element ist vom Typ " **Input**", " **Button**", " **Image** " oder " **Landmark** ", hat aber keinen zugänglichen Namen.</span><span class="sxs-lookup"><span data-stu-id="17140-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="17140-107">type</span><span class="sxs-lookup"><span data-stu-id="17140-107">Type</span></span>

<span data-ttu-id="17140-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="17140-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="17140-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17140-109">Description</span></span>

<span data-ttu-id="17140-110">Dieser Fehler gilt für:</span><span class="sxs-lookup"><span data-stu-id="17140-110">This error applies to:</span></span>

-   <span data-ttu-id="17140-111">Formulareingabe Felder:</span><span class="sxs-lookup"><span data-stu-id="17140-111">Form input fields:</span></span>
    -   <span data-ttu-id="17140-112">HTML-Tags **– \[ Eingabetyp = " \| textkennwort-Kontrollkästchen Optionsfeld- \| \| \| \| e-Mail-Adresse e-Mail-Adresse für \| \| \| \| DateTime \| -Ortszeit-local \| time \| Week \| Month \| Number \| Range \| Search \| \] URL"**, **Select**, **DataList** und **Textarea**.</span><span class="sxs-lookup"><span data-stu-id="17140-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="17140-113">WAI-ARIA-Rollen –**CheckBox**, **ComboBox**, **ListBox**, **Radio Group**, **Radio**, **Textfeld**, **Tree**, **Slider** und **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="17140-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="17140-114">Bilder/Bild-Schaltflächen/-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="17140-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="17140-115">HTML-Tags –**IMG**, **input \[ Type = "Bild Schaltfläche \| " \]** und **Schaltfläche**.</span><span class="sxs-lookup"><span data-stu-id="17140-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="17140-116">Rollen "WAI-ARIA" –**IMG** und **Button**.</span><span class="sxs-lookup"><span data-stu-id="17140-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="17140-117">Besondere Merkmale</span><span class="sxs-lookup"><span data-stu-id="17140-117">Landmarks</span></span>
    -   <span data-ttu-id="17140-118">WAI-ARIA-Rollen –**Region**, **Banner**, **Ergänzung**, **ContentInfo**, **Formular**, **Main**, **Navigation** und **Suche**.</span><span class="sxs-lookup"><span data-stu-id="17140-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="17140-119">Die Zugriffs Prüfung zeigt diesen Fehler auch für Elemente an, für die der barrierefreie Name standardmäßig auf der Grundlage des inneren HTML-Inhalts festgelegt wird (siehe das **Banner** Element im obigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="17140-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="17140-120">In diesen Fällen können Sie diese Fehler unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="17140-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="17140-121">Alle semantisch wichtigen Benutzeroberflächen Elemente, wie z. b. Formularfelder (z. b. **Eingabe**, **Select**, **Textarea**), Bilder, Schaltflächen und Markierungen (Tags, die logische Bereiche darstellen) müssen über den zugreif baren Namen verfügen, damit Bildschirm Sprachausgaben diese korrekt ankündigen können.</span><span class="sxs-lookup"><span data-stu-id="17140-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="17140-122">Um diesen Fehler zu beheben, legen Sie den barrierefreien Namen auf eine der folgenden Weisen fest (in der Reihenfolge der bevorzugte Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="17140-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="17140-123">Formularfelder: Verwenden Sie das Tag **Bezeichnung** , und legen Sie für das Attribut **für** den **ID** -Wert des Zielfelds fest.</span><span class="sxs-lookup"><span data-stu-id="17140-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="17140-124">Bild/Bild-Schaltfläche: Legen Sie das **alt** -Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="17140-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="17140-125">Buttons: Legen Sie den Text der Schaltflächen Beschriftung fest.</span><span class="sxs-lookup"><span data-stu-id="17140-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="17140-126">Für ein beliebiges Element:</span><span class="sxs-lookup"><span data-stu-id="17140-126">For any element:</span></span>
    -   <span data-ttu-id="17140-127">[**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribut: wird auf den **ID** -Wert des Elements festgelegt, das die barrierefreie namens Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="17140-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="17140-128">[**Aria-Label-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) Attribut: auf die barrierefreie namens Zeichenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="17140-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="17140-129">[**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) -Attribut: auf die barrierefreie namens Zeichenfolge festgelegt (außerdem **wird eine** QuickInfo erstellt).</span><span class="sxs-lookup"><span data-stu-id="17140-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="17140-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17140-130">Example</span></span>


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



 

 




