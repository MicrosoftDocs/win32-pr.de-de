---
title: ServiceTask1-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das ServiceTask1-Element stellt den ersten Aufgabenbereich im Online Store dar.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- ServiceTask1-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ca83f5f7935e8d1dfd376f569bd61f68d7e93bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367023"
---
# <a name="servicetask1-element"></a><span data-ttu-id="6fc0d-106">ServiceTask1-Element</span><span class="sxs-lookup"><span data-stu-id="6fc0d-106">ServiceTask1 Element</span></span>

> [!Note]  
> <span data-ttu-id="6fc0d-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="6fc0d-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6fc0d-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6fc0d-109">Das **ServiceTask1** -Element stellt den ersten Aufgabenbereich im Online Store dar.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-109">The **ServiceTask1** element represents the first online store task pane.</span></span>

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="6fc0d-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fc0d-110">Attributes</span></span>



| <span data-ttu-id="6fc0d-111">Begriff</span><span class="sxs-lookup"><span data-stu-id="6fc0d-111">Term</span></span>                                                                                                                             | <span data-ttu-id="6fc0d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fc0d-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6fc0d-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="6fc0d-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="6fc0d-114">Die URL für die Webseite, die von Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6fc0d-115">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="6fc0d-115">Parent/Child Elements</span></span>



| <span data-ttu-id="6fc0d-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="6fc0d-116">Hierarchy</span></span>       | <span data-ttu-id="6fc0d-117">Element</span><span class="sxs-lookup"><span data-stu-id="6fc0d-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="6fc0d-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc0d-118">Parent elements</span></span> | <span data-ttu-id="6fc0d-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="6fc0d-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="6fc0d-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc0d-120">Child elements</span></span>  | <span data-ttu-id="6fc0d-121">**ButtonText**, **buttontip**</span><span class="sxs-lookup"><span data-stu-id="6fc0d-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6fc0d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fc0d-122">Remarks</span></span>

<span data-ttu-id="6fc0d-123">**ServiceTask1** wird als primärer Aufgabenbereich für die Teilnahme an kommerziellen Aktivitäten angesehen.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="6fc0d-124">Dies ist der Aufgabenbereich, der angezeigt wird, wenn der Benutzer sich für den Kauf von Musik entscheidet.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-124">It is the task pane that displays when the user chooses to purchase music.</span></span>

> [!Note]  
> <span data-ttu-id="6fc0d-125">Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-125">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="6fc0d-126">Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-126">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="6fc0d-127">Windows Media Player 11 verfügt nur über einen Aufgabenbereich, der durch **ServiceTask1** dargestellt wird, den der Benutzer durch Klicken auf die Registerkarte **Online Stores** anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-127">Windows Media Player 11 has only one task pane, represented by **ServiceTask1**, which the user can view by clicking on the **Online Stores** tab.</span></span>

 

<span data-ttu-id="6fc0d-128">Aufgabenbereiche im Online Store nutzen eine einzelne Browser Instanz gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-128">Online store task panes share a single browser instance.</span></span> <span data-ttu-id="6fc0d-129">Dies bedeutet, dass Sie auf Ihrer Webseite keinen Skriptcode schreiben sollten, der fortgesetzt werden soll, wenn der Benutzer von der aktuellen Dienst Aufgabe abwechselt.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-129">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="6fc0d-130">Wenn der Benutzer Aufgabenbereiche wechselt, werden die URL-und Sitzungs Cookies in Windows Media Player gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-130">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="6fc0d-131">Wenn der Benutzer wieder zum Aufgabenbereich wechselt, stellt der Spieler die URL und Cookies wieder her.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-131">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="6fc0d-132">Wenn sich der Benutzer für die Verwendung eines anderen Online Stores entscheidet, werden die URL-und Sitzungsdaten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-132">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="6fc0d-133">In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-133">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="6fc0d-134">Andere können für Legacy Kompatibilitätszwecke vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-134">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="6fc0d-135">Name</span><span class="sxs-lookup"><span data-stu-id="6fc0d-135">Name</span></span>         | <span data-ttu-id="6fc0d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc0d-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc0d-137">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="6fc0d-137">*geoid*</span></span>      | <span data-ttu-id="6fc0d-138">ID des geografischen Standorts für Windows.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-138">Windows geographical location ID.</span></span> <span data-ttu-id="6fc0d-139">Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="6fc0d-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="6fc0d-140">*locale*</span></span>     | <span data-ttu-id="6fc0d-141">Windows Media Player-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="6fc0d-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="6fc0d-142">*userlocale*</span></span> | <span data-ttu-id="6fc0d-143">Windows-Gebiets Schema-ID.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-143">Windows locale ID.</span></span> <span data-ttu-id="6fc0d-144">Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="6fc0d-145">*version*</span><span class="sxs-lookup"><span data-stu-id="6fc0d-145">*version*</span></span>    | <span data-ttu-id="6fc0d-146">Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="6fc0d-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc0d-147">Requirements</span></span>



| <span data-ttu-id="6fc0d-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc0d-148">Requirement</span></span> | <span data-ttu-id="6fc0d-149">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc0d-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="6fc0d-150">Version</span><span class="sxs-lookup"><span data-stu-id="6fc0d-150">Version</span></span><br/> | <span data-ttu-id="6fc0d-151">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="6fc0d-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fc0d-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc0d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc0d-153">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="6fc0d-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="6fc0d-154">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="6fc0d-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="6fc0d-155">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="6fc0d-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





