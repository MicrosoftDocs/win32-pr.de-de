---
description: Veranschaulicht, wie eine benutzerdefinierte Sprung Liste für eine Anwendung erstellt wird, einschließlich Hinzufügen einer benutzerdefinierten Kategorie und Aufgaben.
title: Benutzerdefinierte Sprungliste (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217206"
---
# <a name="custom-jump-list-sample"></a><span data-ttu-id="0d24c-103">Benutzerdefinierte Sprungliste (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="0d24c-103">Custom Jump List Sample</span></span>

<span data-ttu-id="0d24c-104">Veranschaulicht, wie eine benutzerdefinierte Sprung Liste für eine Anwendung erstellt wird, einschließlich Hinzufügen einer benutzerdefinierten Kategorie und Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="0d24c-104">Demonstrates how to create a custom Jump List for an application, including adding a custom category and tasks.</span></span>

<span data-ttu-id="0d24c-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="0d24c-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0d24c-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d24c-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0d24c-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0d24c-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0d24c-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="0d24c-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0d24c-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0d24c-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0d24c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d24c-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0d24c-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0d24c-111">Requirements</span></span>



| <span data-ttu-id="0d24c-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="0d24c-112">Product</span></span>                                | <span data-ttu-id="0d24c-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="0d24c-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="0d24c-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0d24c-114">Windows</span></span>                                | <span data-ttu-id="0d24c-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d24c-115">Windows 7</span></span>               |
| <span data-ttu-id="0d24c-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="0d24c-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="0d24c-117">7.0</span><span class="sxs-lookup"><span data-stu-id="0d24c-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0d24c-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0d24c-118">Downloading the Sample</span></span>

| <span data-ttu-id="0d24c-119">Standort</span><span class="sxs-lookup"><span data-stu-id="0d24c-119">Location</span></span>      | <span data-ttu-id="0d24c-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="0d24c-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d24c-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="0d24c-121">GitHub</span></span>  | [<span data-ttu-id="0d24c-122">Customjumplist-Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d24c-122">CustomJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="0d24c-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0d24c-123">Building the Sample</span></span>

<span data-ttu-id="0d24c-124">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="0d24c-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="0d24c-125">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **customjumplist** .</span><span class="sxs-lookup"><span data-stu-id="0d24c-125">Open the command prompt window and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="0d24c-126">Geben Sie `msbuild CustomJumpListSample.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="0d24c-126">Enter `msbuild CustomJumpListSample.sln`.</span></span>

<span data-ttu-id="0d24c-127">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="0d24c-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0d24c-128">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **customjumplist** .</span><span class="sxs-lookup"><span data-stu-id="0d24c-128">Open Windows Explorer and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="0d24c-129">Doppelklicken Sie auf das Symbol für die Datei customjumplistsample. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0d24c-129">Double-click the icon for the CustomJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="0d24c-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d24c-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0d24c-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0d24c-131">Running the Sample</span></span>

1.  <span data-ttu-id="0d24c-132">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="0d24c-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="0d24c-133">Geben Sie in der Befehlszeile ein `CustomJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="0d24c-133">At the command line, enter `CustomJumpListSample.exe`.</span></span> <span data-ttu-id="0d24c-134">Alternativ können Sie in Windows-Explorer auf das Symbol für CustomJumpListSample.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="0d24c-134">Alternatively, from Windows Explorer double-click the icon for CustomJumpListSample.exe.</span></span>
3.  <span data-ttu-id="0d24c-135">Dieses Beispiel muss bei der erstmaligen Durchführung als Administrator ausgeführt werden, damit die erforderlichen Dateityp Registrierungen installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="0d24c-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="0d24c-136">Nachdem die Dateitypen registriert wurden, kann das Beispiel als Standardbenutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d24c-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="0d24c-137">Wählen Sie Optionen aus dem Menü in der Beispielanwendung aus, um zu sehen, wie Sie sich auf die Sprung Liste der Anwendung in der Taskleiste auswirken.</span><span class="sxs-lookup"><span data-stu-id="0d24c-137">Select options from the menu in the sample application to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d24c-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d24c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d24c-139">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="0d24c-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



