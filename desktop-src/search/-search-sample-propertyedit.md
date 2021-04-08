---
description: Das propertyedit-Codebeispiel veranschaulicht, wie Sie den kanonischen Eigenschaftsnamen in einen PropertyKey konvertieren, den Wert des Eigenschaften Speicher auf den des Elements festlegen und die Daten zurück in den Dateistream schreiben.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862167"
---
# <a name="propertyedit"></a><span data-ttu-id="302c5-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="302c5-103">PropertyEdit</span></span>

<span data-ttu-id="302c5-104">Das propertyedit-Codebeispiel veranschaulicht, wie Sie den kanonischen Eigenschaftsnamen in einen PropertyKey konvertieren, den Wert des Eigenschaften Speicher auf den des Elements festlegen und die Daten zurück in den Dateistream schreiben.</span><span class="sxs-lookup"><span data-stu-id="302c5-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="302c5-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="302c5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="302c5-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="302c5-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="302c5-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="302c5-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="302c5-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="302c5-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="302c5-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="302c5-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="302c5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="302c5-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="302c5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="302c5-111">Requirements</span></span>



| <span data-ttu-id="302c5-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="302c5-112">Product</span></span>     | <span data-ttu-id="302c5-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="302c5-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="302c5-114">Windows</span><span class="sxs-lookup"><span data-stu-id="302c5-114">Windows</span></span>     | <span data-ttu-id="302c5-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="302c5-115">Windows 7</span></span>               |
| <span data-ttu-id="302c5-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="302c5-116">Windows SDK</span></span> | <span data-ttu-id="302c5-117">7.0</span><span class="sxs-lookup"><span data-stu-id="302c5-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="302c5-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="302c5-118">Downloading the Sample</span></span>

<span data-ttu-id="302c5-119">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="302c5-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="302c5-120">Standort</span><span class="sxs-lookup"><span data-stu-id="302c5-120">Location</span></span>      | <span data-ttu-id="302c5-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="302c5-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="302c5-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="302c5-122">GitHub</span></span>  | [<span data-ttu-id="302c5-123">Propertyedit-Beispiel</span><span class="sxs-lookup"><span data-stu-id="302c5-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="302c5-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="302c5-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="302c5-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="302c5-125">Building the Sample</span></span>

<span data-ttu-id="302c5-126">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="302c5-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="302c5-127">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **propertyedit** .</span><span class="sxs-lookup"><span data-stu-id="302c5-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="302c5-128">Geben Sie `msbuild PropertyEdit.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="302c5-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="302c5-129">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="302c5-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="302c5-130">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **propertyedit** .</span><span class="sxs-lookup"><span data-stu-id="302c5-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="302c5-131">Doppelklicken Sie auf das Symbol für die Datei propertyedit. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="302c5-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="302c5-132">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="302c5-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="302c5-133">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="302c5-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="302c5-134">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="302c5-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="302c5-135">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="302c5-135">Running the Sample</span></span>

1.  <span data-ttu-id="302c5-136">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="302c5-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="302c5-137">Geben Sie an der Eingabeaufforderung ein, `PropertyEdit.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für PropertyEdit.exe.</span><span class="sxs-lookup"><span data-stu-id="302c5-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="302c5-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="302c5-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="302c5-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="302c5-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="302c5-140">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="302c5-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="302c5-141">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="302c5-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="302c5-142">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="302c5-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="302c5-143">Informationen zu Eigenschaften und Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="302c5-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="302c5-144">[Eigenschafts Beschreibungs Schema](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="302c5-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 
