---
description: Veranschaulicht das Hinzufügen von Elementen zur automatischen Sprung Liste für eine Anwendung, einschließlich des Wechsels zwischen der Anzeige der häufig und der aktuellen Kategorie.
title: Beispiel für eine automatische Sprungliste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485563"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="3c209-103">Beispiel für eine automatische Sprungliste</span><span class="sxs-lookup"><span data-stu-id="3c209-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="3c209-104">Veranschaulicht das Hinzufügen von Elementen zur automatischen Sprung Liste für eine Anwendung, einschließlich des Wechsels zwischen der Anzeige der häufig und der aktuellen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="3c209-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="3c209-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3c209-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3c209-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c209-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3c209-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3c209-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3c209-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="3c209-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3c209-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3c209-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="3c209-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c209-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="3c209-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3c209-111">Requirements</span></span>



| <span data-ttu-id="3c209-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="3c209-112">Product</span></span>                                | <span data-ttu-id="3c209-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="3c209-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3c209-114">Windows</span><span class="sxs-lookup"><span data-stu-id="3c209-114">Windows</span></span>                                | <span data-ttu-id="3c209-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c209-115">Windows 7</span></span>               |
| <span data-ttu-id="3c209-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="3c209-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3c209-117">7.0</span><span class="sxs-lookup"><span data-stu-id="3c209-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3c209-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3c209-118">Downloading the Sample</span></span>

| <span data-ttu-id="3c209-119">Standort</span><span class="sxs-lookup"><span data-stu-id="3c209-119">Location</span></span>      | <span data-ttu-id="3c209-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="3c209-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c209-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="3c209-121">GitHub</span></span>  | [<span data-ttu-id="3c209-122">Automaticjumplist-Beispiel</span><span class="sxs-lookup"><span data-stu-id="3c209-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="3c209-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3c209-123">Building the Sample</span></span>

<span data-ttu-id="3c209-124">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="3c209-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="3c209-125">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **automaticjumplist** .</span><span class="sxs-lookup"><span data-stu-id="3c209-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="3c209-126">Geben Sie `msbuild AutomaticJumpListSample.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="3c209-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="3c209-127">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="3c209-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="3c209-128">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **automaticjumplist** .</span><span class="sxs-lookup"><span data-stu-id="3c209-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="3c209-129">Doppelklicken Sie auf das Symbol für die Datei automaticjumplistsample. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3c209-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3c209-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="3c209-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3c209-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3c209-131">Running the Sample</span></span>

1.  <span data-ttu-id="3c209-132">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="3c209-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="3c209-133">Geben Sie in der Befehlszeile ein `AutomaticJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="3c209-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="3c209-134">Alternativ können Sie in Windows-Explorer auf das Symbol für AutomaticJumpListSample.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="3c209-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="3c209-135">Dieses Beispiel muss bei der erstmaligen Durchführung als Administrator ausgeführt werden, damit die erforderlichen Dateityp Registrierungen installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="3c209-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="3c209-136">Nachdem die Dateitypen registriert wurden, kann das Beispiel als Standardbenutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c209-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="3c209-137">Wählen Sie Optionen aus dem Menü in der Beispielanwendung aus, einschließlich der Auswahl von txt-oder doc-Dokumenten über das Dialogfeld **Öffnen** , um zu sehen, wie Sie sich auf die Sprung Liste der Anwendung in der Taskleiste auswirken.</span><span class="sxs-lookup"><span data-stu-id="3c209-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c209-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c209-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c209-139">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="3c209-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



