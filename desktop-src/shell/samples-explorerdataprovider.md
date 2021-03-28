---
description: Veranschaulicht, wie eine Shell-Namespace Erweiterung implementiert wird, einschließlich Kontextmenü Verhalten und benutzerdefinierter Aufgaben im Browser.
title: Explorer-Datenanbieter (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218062"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="b9eda-103">Explorer-Datenanbieter (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="b9eda-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="b9eda-104">Veranschaulicht, wie eine Shell-Namespace Erweiterung implementiert wird, einschließlich Kontextmenü Verhalten und benutzerdefinierter Aufgaben im Browser.</span><span class="sxs-lookup"><span data-stu-id="b9eda-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="b9eda-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b9eda-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b9eda-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9eda-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b9eda-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b9eda-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b9eda-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="b9eda-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b9eda-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b9eda-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="b9eda-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b9eda-110">Requirements</span></span>



| <span data-ttu-id="b9eda-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="b9eda-111">Product</span></span>                                | <span data-ttu-id="b9eda-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="b9eda-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b9eda-113">Windows</span><span class="sxs-lookup"><span data-stu-id="b9eda-113">Windows</span></span>                                | <span data-ttu-id="b9eda-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9eda-114">Windows Vista</span></span>           |
| <span data-ttu-id="b9eda-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b9eda-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b9eda-116">6.1</span><span class="sxs-lookup"><span data-stu-id="b9eda-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b9eda-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b9eda-117">Downloading the Sample</span></span>

| <span data-ttu-id="b9eda-118">Standort</span><span class="sxs-lookup"><span data-stu-id="b9eda-118">Location</span></span>      | <span data-ttu-id="b9eda-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="b9eda-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9eda-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="b9eda-120">GitHub</span></span>  | [<span data-ttu-id="b9eda-121">Explorerdataprovider-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b9eda-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="b9eda-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b9eda-122">Building the Sample</span></span>

<span data-ttu-id="b9eda-123">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="b9eda-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="b9eda-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **explorerdataprovider** .</span><span class="sxs-lookup"><span data-stu-id="b9eda-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="b9eda-125">Geben Sie `msbuild ExplorerDataProvider.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="b9eda-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="b9eda-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="b9eda-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="b9eda-127">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **explorerdataprovider** .</span><span class="sxs-lookup"><span data-stu-id="b9eda-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="b9eda-128">Doppelklicken Sie auf das Symbol für die Datei explorerdataprovider. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b9eda-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b9eda-129">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b9eda-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="b9eda-130">Die dll wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="b9eda-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="b9eda-131">In der Version dieses Beispiels, das in der Windows SDK enthalten ist, enthält die Konfiguration für den Build der 64-Bit-Version nicht die Datei "explorerdataprovider. def" in der **Modul Definitionsdatei** -Option des Linkers.</span><span class="sxs-lookup"><span data-stu-id="b9eda-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="b9eda-132">Sie müssen diese Datei vor dem Aufbau in einer 64-Bit-Umgebung selbst angeben.</span><span class="sxs-lookup"><span data-stu-id="b9eda-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="b9eda-133">Fügen Sie die Zeile `ModuleDefinitionFile="ExplorerDataProvider.def"` zum Abschnitt "VCLinkerTool" (beginnt in Zeile 329) der Datei "explorerdataprovider. vcproj" hinzu, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b9eda-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="b9eda-134">Die Version dieses Beispiels, die aus der Code Gallery heruntergeladen werden kann, wurde für dieses Problem korrigiert, und es sind keine weiteren Aktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b9eda-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="b9eda-135">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b9eda-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="b9eda-136">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue dll-und PropDesc-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="b9eda-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="b9eda-137">Geben Sie in der Befehlszeile ein `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="b9eda-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="b9eda-138">Wenn Sie diesen Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausführen, wird die Datei ". PropDesc" auch automatisch von der Selbstregistrierung registriert.</span><span class="sxs-lookup"><span data-stu-id="b9eda-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="b9eda-139">Wenn Sie an einer Eingabeaufforderung ohne erhöhte Rechte ausgeführt wird, funktioniert die Namespace Erweiterung, aber ohne benutzerdefinierte Eigenschafts Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="b9eda-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="b9eda-140">Öffnen Sie den Ordner **Arbeitsplatz** , und Durchsuchen Sie die neue Namespace Erweiterung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b9eda-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>


