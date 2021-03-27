---
description: Veranschaulicht das Schreiben eines Handlers, der zum Anzeigen einer Datei Vorschau innerhalb des Vorschau Bereichs von Windows-Explorer oder anderen Vorschau handlerhosts verwendet wird.
title: Rezept-Vorschauhandler (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980248"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="9b353-103">Rezept-Vorschauhandler (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="9b353-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="9b353-104">Veranschaulicht das Schreiben eines Handlers, der zum Anzeigen einer Datei Vorschau innerhalb des Vorschau Bereichs von Windows-Explorer oder anderen Vorschau handlerhosts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b353-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="9b353-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9b353-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9b353-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b353-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9b353-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9b353-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9b353-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="9b353-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9b353-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9b353-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="9b353-110">Aufheben der Registrierung der Beispiel-Vorschau Handler-dll</span><span class="sxs-lookup"><span data-stu-id="9b353-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="9b353-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b353-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="9b353-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9b353-112">Requirements</span></span>



| <span data-ttu-id="9b353-113">Produkt</span><span class="sxs-lookup"><span data-stu-id="9b353-113">Product</span></span>                                | <span data-ttu-id="9b353-114">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="9b353-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9b353-115">Windows</span><span class="sxs-lookup"><span data-stu-id="9b353-115">Windows</span></span>                                | <span data-ttu-id="9b353-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b353-116">Windows Vista</span></span>           |
| <span data-ttu-id="9b353-117">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="9b353-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="9b353-118">7.0</span><span class="sxs-lookup"><span data-stu-id="9b353-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9b353-119">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9b353-119">Downloading the Sample</span></span>

| <span data-ttu-id="9b353-120">Standort</span><span class="sxs-lookup"><span data-stu-id="9b353-120">Location</span></span>      | <span data-ttu-id="9b353-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="9b353-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b353-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="9b353-122">GitHub</span></span>  | [<span data-ttu-id="9b353-123">Beispiel für "recipeer PreviewHandler"</span><span class="sxs-lookup"><span data-stu-id="9b353-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="9b353-124">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9b353-124">Building the Sample</span></span>

<span data-ttu-id="9b353-125">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="9b353-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="9b353-126">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis " **recipeer PreviewHandler** ".</span><span class="sxs-lookup"><span data-stu-id="9b353-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="9b353-127">Beispiel: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="9b353-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="9b353-128">Geben Sie `msbuild PreviewHandlerSDKSample.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="9b353-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="9b353-129">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="9b353-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="9b353-130">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **recipeer PreviewHandler** ".</span><span class="sxs-lookup"><span data-stu-id="9b353-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="9b353-131">Doppelklicken Sie auf das Symbol für die Datei previewhandlersdksample. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9b353-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="9b353-132">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b353-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="9b353-133">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9b353-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="9b353-134">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9b353-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="9b353-135">Wenn das Zielsystem 64-Bit (x64) ist, muss dieser Beispiel-Vorschau Handler als 64-Bit-Anwendung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b353-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="9b353-136">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9b353-136">Running the Sample</span></span>

1.  <span data-ttu-id="9b353-137">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum erstellten Projektverzeichnis " **recipeer PreviewHandler** ".</span><span class="sxs-lookup"><span data-stu-id="9b353-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="9b353-138">Beispiel: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="9b353-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="9b353-139">Geben Sie ein `regsvr32.exe PreviewHandlerSDKSample.dll` , um den Handler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="9b353-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="9b353-140">Öffnen Sie Windows-Explorer, und zeigen Sie den Vorschaubereich an, wenn er nicht bereits angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b353-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="9b353-141">**Windows 7**: Klicken Sie auf die Schaltfläche Vorschaubereich.</span><span class="sxs-lookup"><span data-stu-id="9b353-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="9b353-142">**Windows Vista**: Klicken Sie auf das Menü **organisieren** , wechseln Sie zum Untermenü **Layout** , und wählen Sie **Vorschau** Bereich aus.</span><span class="sxs-lookup"><span data-stu-id="9b353-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="9b353-143">Navigieren Sie in Windows-Explorer zum Projektverzeichnis " **recipeer PreviewHandler** ".</span><span class="sxs-lookup"><span data-stu-id="9b353-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="9b353-144">Wählen Sie die Datei "example. Rezept" aus.</span><span class="sxs-lookup"><span data-stu-id="9b353-144">Select the example .recipe file.</span></span>

<span data-ttu-id="9b353-145">Legen Sie den **AppID** -Wert `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` wie im folgenden Code gezeigt auf den WOW64-Ersatz Zeichen Host fest, damit sowohl die 32-Bit (x86)-als auch die 64-Bit (x64)-Ausgabe in einer 64-Bit-Version von Windows funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9b353-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="9b353-146">Aufheben der Registrierung der Beispiel-Vorschau Handler-dll</span><span class="sxs-lookup"><span data-stu-id="9b353-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="9b353-147">Öffnen Sie die Eingabeaufforderung, und geben Sie ein `regsvr32.exe /u PreviewHandlerSDKSample.dll` , um die Registrierung des Handlers aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="9b353-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b353-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b353-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b353-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="9b353-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="9b353-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="9b353-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="9b353-151">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="9b353-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
