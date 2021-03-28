---
description: Veranschaulicht, wie das Verhalten der Task leisten Gruppierung der Fenster einer Anwendung über die System.AppUserModel.ID-Eigenschaft gesteuert wird.
title: Fenstereigenschaft „Anwendungsbenutzermodell-ID“ (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980344"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="2d312-103">Beispiel für eine Anwendungs Benutzer Modell-ID (AppID) Window-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d312-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="2d312-104">Veranschaulicht, wie das Verhalten der Task leisten Gruppierung der Fenster einer Anwendung über die [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="2d312-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="2d312-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="2d312-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2d312-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d312-106">Description</span></span>](#description)
-   [<span data-ttu-id="2d312-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d312-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2d312-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2d312-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2d312-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="2d312-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2d312-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2d312-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="2d312-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d312-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="2d312-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d312-112">Description</span></span>

<span data-ttu-id="2d312-113">Dieses Beispiel zeigt, wie die [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft mithilfe der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Implementierung des Fensters festgelegt wird, die über [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2d312-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d312-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2d312-114">Requirements</span></span>



| <span data-ttu-id="2d312-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="2d312-115">Product</span></span>                                | <span data-ttu-id="2d312-116">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="2d312-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="2d312-117">Windows</span><span class="sxs-lookup"><span data-stu-id="2d312-117">Windows</span></span>                                | <span data-ttu-id="2d312-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d312-118">Windows 7</span></span>               |
| <span data-ttu-id="2d312-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="2d312-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="2d312-120">7.0</span><span class="sxs-lookup"><span data-stu-id="2d312-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2d312-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2d312-121">Downloading the Sample</span></span>

| <span data-ttu-id="2d312-122">Standort</span><span class="sxs-lookup"><span data-stu-id="2d312-122">Location</span></span>      | <span data-ttu-id="2d312-123">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="2d312-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d312-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="2d312-124">GitHub</span></span>  | [<span data-ttu-id="2d312-125">Appusermudelidwindowproperty-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2d312-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="2d312-126">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2d312-126">Building the Sample</span></span>

<span data-ttu-id="2d312-127">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="2d312-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="2d312-128">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **appusermudelidwindowproperty** .</span><span class="sxs-lookup"><span data-stu-id="2d312-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="2d312-129">Geben Sie `msbuild AppUserModelIDWindowProperty.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="2d312-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="2d312-130">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="2d312-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="2d312-131">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **appusermudelidwindowproperty** ".</span><span class="sxs-lookup"><span data-stu-id="2d312-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="2d312-132">Doppelklicken Sie auf das Symbol für die Datei appusermudelidwindowproperty. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2d312-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="2d312-133">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="2d312-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2d312-134">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2d312-134">Running the Sample</span></span>

1.  <span data-ttu-id="2d312-135">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="2d312-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="2d312-136">Geben Sie in der Befehlszeile ein `AppUserModelIDWindowProperty.exe` .</span><span class="sxs-lookup"><span data-stu-id="2d312-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="2d312-137">Alternativ können Sie in Windows-Explorer auf das Symbol für AppUserModelIDWindowProperty.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="2d312-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="2d312-138">Um zu veranschaulichen, wie sich die App-Benutzer Modell-IDs (appusermudelids) auf die Task leisten Gruppierung auswirken, starten Sie mindestens drei Instanzen der Anwendung gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="2d312-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="2d312-139">Verwenden Sie das Menü, um für jedes der drei Fenster eine andere appusermodelid festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2d312-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="2d312-140">Beachten Sie, dass jede separate appusermodelid zu einer separaten Task leisten Schaltfläche führt und dass Windows Ihre Identität zur Laufzeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="2d312-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="2d312-141">Legen Sie mindestens zwei Fenster auf die zweite appusermodelid fest.</span><span class="sxs-lookup"><span data-stu-id="2d312-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="2d312-142">Beachten Sie, dass beide in dieselbe Task leisten Gruppe verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="2d312-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="2d312-143">Öffnen Sie das Fenster **Taskleiste und Start Menü Eigenschaften** , indem Sie mit der rechten Maustaste auf die Taskleiste klicken und im Kontextmenü **Eigenschaften** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2d312-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="2d312-144">Ändern der **Task** leisten Schaltflächen: Dropdown zwischen der **Kombination, wenn die Taskleiste voll ist** und **nie Werte kombinieren** .</span><span class="sxs-lookup"><span data-stu-id="2d312-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="2d312-145">Beachten Sie, dass jedes Fenster eine separate Schaltfläche erhalten kann, dass die Schaltflächen jedoch nach appusermodelid gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="2d312-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d312-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d312-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d312-147">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="2d312-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
