---
title: ServiceTask2-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das ServiceTask2-Element stellt den zweiten Aufgabenbereich im Online Store dar.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- ServiceTask2-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36052dabc1be7f2925f5185239faa602b8633fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374002"
---
# <a name="servicetask2-element"></a><span data-ttu-id="3d888-106">ServiceTask2-Element</span><span class="sxs-lookup"><span data-stu-id="3d888-106">ServiceTask2 Element</span></span>

> [!Note]  
> <span data-ttu-id="3d888-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="3d888-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3d888-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d888-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3d888-109">Das **ServiceTask2** -Element stellt den zweiten Aufgabenbereich im Online Store dar.</span><span class="sxs-lookup"><span data-stu-id="3d888-109">The **ServiceTask2** element represents the second online store task pane.</span></span>

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="3d888-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d888-110">Attributes</span></span>



| <span data-ttu-id="3d888-111">Begriff</span><span class="sxs-lookup"><span data-stu-id="3d888-111">Term</span></span>                                                                                                                             | <span data-ttu-id="3d888-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d888-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3d888-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="3d888-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="3d888-114">Die URL für die Webseite, die von Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3d888-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="3d888-115">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="3d888-115">Parent/Child Elements</span></span>



| <span data-ttu-id="3d888-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="3d888-116">Hierarchy</span></span>       | <span data-ttu-id="3d888-117">Element</span><span class="sxs-lookup"><span data-stu-id="3d888-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="3d888-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d888-118">Parent elements</span></span> | <span data-ttu-id="3d888-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="3d888-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="3d888-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d888-120">Child elements</span></span>  | <span data-ttu-id="3d888-121">**ButtonText**, **buttontip**</span><span class="sxs-lookup"><span data-stu-id="3d888-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3d888-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d888-122">Remarks</span></span>

<span data-ttu-id="3d888-123">**ServiceTask1** wird als primärer Aufgabenbereich für die Teilnahme an kommerziellen Aktivitäten angesehen.</span><span class="sxs-lookup"><span data-stu-id="3d888-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="3d888-124">Dies ist der Aufgabenbereich, der angezeigt wird, wenn der Benutzer sich für den Kauf von Musik entscheidet.</span><span class="sxs-lookup"><span data-stu-id="3d888-124">It is the task pane that displays when the user chooses to purchase music.</span></span> <span data-ttu-id="3d888-125">Verwenden Sie **ServiceTask2** für andere Online Store-Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="3d888-125">Use **ServiceTask2** for other online store activity.</span></span>

> [!Note]  
> <span data-ttu-id="3d888-126">Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="3d888-126">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="3d888-127">Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d888-127">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="3d888-128">Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer durch Klicken auf die Registerkarte " **Online Stores** " anzeigen kann. die **ServiceTask2** -und **ServiceTask3** -Elemente werden von Windows Media Player 11 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3d888-128">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="3d888-129">Online Store-Aufgabenbereiche nutzen eine einzelne Browser Instanz gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="3d888-129">Online stores task panes share a single browser instance.</span></span> <span data-ttu-id="3d888-130">Dies bedeutet, dass Sie auf Ihrer Webseite keinen Skriptcode schreiben sollten, der fortgesetzt werden soll, wenn der Benutzer von der aktuellen Dienst Aufgabe abwechselt.</span><span class="sxs-lookup"><span data-stu-id="3d888-130">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="3d888-131">Wenn der Benutzer Aufgabenbereiche wechselt, werden die URL-und Sitzungs Cookies in Windows Media Player gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3d888-131">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="3d888-132">Wenn der Benutzer wieder zum Aufgabenbereich wechselt, stellt der Spieler die URL und Cookies wieder her.</span><span class="sxs-lookup"><span data-stu-id="3d888-132">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="3d888-133">Wenn sich der Benutzer für die Verwendung eines anderen Online Stores entscheidet, werden die URL-und Sitzungsdaten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3d888-133">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="3d888-134">In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="3d888-134">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="3d888-135">Andere können für Legacy Kompatibilitätszwecke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3d888-135">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="3d888-136">Name</span><span class="sxs-lookup"><span data-stu-id="3d888-136">Name</span></span>         | <span data-ttu-id="3d888-137">Wert</span><span class="sxs-lookup"><span data-stu-id="3d888-137">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d888-138">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="3d888-138">*geoid*</span></span>      | <span data-ttu-id="3d888-139">ID des geografischen Standorts für Windows.</span><span class="sxs-lookup"><span data-stu-id="3d888-139">Windows geographical location ID.</span></span> <span data-ttu-id="3d888-140">Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d888-140">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="3d888-141">*locale*</span><span class="sxs-lookup"><span data-stu-id="3d888-141">*locale*</span></span>     | <span data-ttu-id="3d888-142">Windows Media Player-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="3d888-142">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="3d888-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="3d888-143">*userlocale*</span></span> | <span data-ttu-id="3d888-144">Windows-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="3d888-144">Windows locale ID.</span></span> <span data-ttu-id="3d888-145">Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d888-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="3d888-146">*version*</span><span class="sxs-lookup"><span data-stu-id="3d888-146">*version*</span></span>    | <span data-ttu-id="3d888-147">Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="3d888-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="3d888-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d888-148">Requirements</span></span>



| <span data-ttu-id="3d888-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d888-149">Requirement</span></span> | <span data-ttu-id="3d888-150">Wert</span><span class="sxs-lookup"><span data-stu-id="3d888-150">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="3d888-151">Version</span><span class="sxs-lookup"><span data-stu-id="3d888-151">Version</span></span><br/> | <span data-ttu-id="3d888-152">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="3d888-152">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d888-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d888-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d888-154">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="3d888-154">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="3d888-155">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="3d888-155">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="3d888-156">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="3d888-156">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





