---
title: Registrieren eines Dienstanbieter
description: Wenn Sie Ihren Dienst der Liste der Anbieter im Webpublishing-Assistenten oder im Assistenten für die Online-druckbestellung hinzufügen möchten, müssen Sie den entsprechenden Schlüssel und seine Werte der Windows-Registrierung hinzufügen.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrieren, Dienste
- Webpublishing-Assistent, registrieren
- Online-druckstellungs-Assistent, registrieren
- registrieren, Webpublishing-Assistent
- registrieren, Assistent für Online-Druck Bestellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219407"
---
# <a name="registering-a-service"></a><span data-ttu-id="8e63c-108">Registrieren eines Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8e63c-108">Registering a Service</span></span>

<span data-ttu-id="8e63c-109">Wenn Sie Ihren Dienst der Liste der Anbieter im Webpublishing-Assistenten oder im Assistenten für die Online-druckbestellung hinzufügen möchten, müssen Sie den entsprechenden Schlüssel und seine Werte der Windows-Registrierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e63c-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="8e63c-110">Erforderliche Schlüssel und Werte</span><span class="sxs-lookup"><span data-stu-id="8e63c-110">Required Keys and Values</span></span>

<span data-ttu-id="8e63c-111">Fügen Sie einen Schlüssel hinzu, wie unten gezeigt, um den Dienst der Liste der Anbieter für den Webpublishing-Assistenten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e63c-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="8e63c-112">Fügen Sie einen Schlüssel hinzu, wie unten gezeigt, um den Dienst der Liste der Anbieter für den Online-druckstellungs-Assistenten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e63c-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="8e63c-113">Jeder Wert ist eine Zeichenfolge vom Typ reg \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="8e63c-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="8e63c-114">Stellen Sie die Daten wie in der folgenden Tabelle erläutert bereit.</span><span class="sxs-lookup"><span data-stu-id="8e63c-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="8e63c-115">Wertname</span><span class="sxs-lookup"><span data-stu-id="8e63c-115">Value Name</span></span>     | <span data-ttu-id="8e63c-116">Erklärung</span><span class="sxs-lookup"><span data-stu-id="8e63c-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e63c-117">IconPath</span><span class="sxs-lookup"><span data-stu-id="8e63c-117">IconPath</span></span>       | <span data-ttu-id="8e63c-118">Der vollständige Pfad zur Symbol Datei, einschließlich des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="8e63c-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8e63c-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e63c-119">DisplayName</span></span>    | <span data-ttu-id="8e63c-120">Der Name, der für Ihren Dienst in der Anbieterliste des Assistenten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8e63c-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8e63c-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e63c-121">Description</span></span>    | <span data-ttu-id="8e63c-122">Eine kurze Beschreibung für Ihren Dienst.</span><span class="sxs-lookup"><span data-stu-id="8e63c-122">A short description for your service.</span></span> <span data-ttu-id="8e63c-123">Diese Beschreibung wird auch in der Anbieterliste des Assistenten direkt unterhalb des Namens Ihres Dienstanbietern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e63c-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8e63c-124">HREF</span><span class="sxs-lookup"><span data-stu-id="8e63c-124">HREF</span></span>           | <span data-ttu-id="8e63c-125">Die URL der ersten Seite Ihres Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8e63c-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8e63c-126">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="8e63c-126">SupportedTypes</span></span> | <span data-ttu-id="8e63c-127">Die von Ihrem Dienst unterstützten Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="8e63c-127">The file types supported by your service.</span></span> <span data-ttu-id="8e63c-128">Beispielsweise *\* . jpg*.</span><span class="sxs-lookup"><span data-stu-id="8e63c-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="8e63c-129">Wenn Sie nur bestimmte Dateitypen angeben, wird der Dienst nur angezeigt, wenn diese Dateitypen ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="8e63c-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="8e63c-130">Wenn mehr als ein Dateityp ausgewählt wurde, wird der Dienst angezeigt, wenn einer dieser Dateitypen von Ihrem Dienst unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8e63c-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="8e63c-131">Wenn Sie mehrere Dateitypen angeben möchten, trennen Sie diese durch Semikolons in der Liste.</span><span class="sxs-lookup"><span data-stu-id="8e63c-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="8e63c-132">Beispiel: *\* . jpg; \* . BMP*.</span><span class="sxs-lookup"><span data-stu-id="8e63c-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="8e63c-133">Im folgenden finden Sie ein umfassendes Beispiel für einen fotoverarbeitungs Dienst mit dem Namen "MyProvider".</span><span class="sxs-lookup"><span data-stu-id="8e63c-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="8e63c-134">Wenn die URL des Dienes aufgerufen wird, werden zwei Werte am Ende der URL – LCID und langid hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8e63c-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="8e63c-135">Beispielsweise könnte die URL-Zeichenfolge für das obige Beispiel https: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&langid = 1033 lauten.</span><span class="sxs-lookup"><span data-stu-id="8e63c-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="8e63c-136">Diese Variablen werden für Sprach-und Lokalisierungs Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e63c-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="8e63c-137">**LCID** wird verwendet, um den Server über die Land-/Regions-und Spracheinstellungen des Clients zu informieren.</span><span class="sxs-lookup"><span data-stu-id="8e63c-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="8e63c-138">Er wird nicht verwendet, um die Sprache der Benutzeroberfläche des Clients zu bestimmen. er wird jedoch verwendet, um das richtige Format für Währung, Datum und Uhrzeit und andere regionsspezifische Daten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8e63c-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="8e63c-139">**LangID** wird verwendet, um den Server über die Standard Spracheinstellung des Clients zu informieren, sodass die richtige Sprache in der Benutzeroberfläche verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e63c-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




