---
description: In diesem Thema wird beschrieben, wie eine typische MUI-Anwendung erstellt wird.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Lokalisieren von Ressourcen und entwickeln der Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345183"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="dd085-103">Lokalisieren von Ressourcen und entwickeln der Anwendung</span><span class="sxs-lookup"><span data-stu-id="dd085-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="dd085-104">In diesem Thema wird beschrieben, wie eine typische MUI-Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dd085-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="dd085-105">Es wird davon ausgegangen, dass Sie Microsoft Visual Studio für die Codierung verwenden und entweder Microsoft Visual Studio oder die Visual Studio-Befehlszeile für die Erstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd085-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="dd085-106">Es wird davon ausgegangen, dass Sie eine sln-Projektmappendatei für Ihre Anwendung verwenden und eine Resource. h-Datei unterstützen, um die Ressourcen Datei der Basis Sprache widerzuspiegeln</span><span class="sxs-lookup"><span data-stu-id="dd085-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="dd085-107">Wenn Sie die Visual Studio-Befehlszeile für den Build verwenden, verwenden Sie den **VCBuild** -Befehl, um die Projektmappendatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd085-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="dd085-108">Anwendungs Dateien werden separat für jede Sprache erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd085-108">Application files are built separately for each language.</span></span> <span data-ttu-id="dd085-109">Jeder Build erstellt identische sprachneutrale. exe-und sprachspezifische. exe. MUI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="dd085-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="dd085-110">Außerdem werden verschiedene andere Dateien in die entsprechenden releaseordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="dd085-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="dd085-111">Der anwendungsbuild hängt von der Art der Ressourcen und von der Art der Lokalisierung ab, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd085-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="dd085-112">Bei der präbuildlokalisierung haben Sie eine Kopie der Basis Sprachdatei für jede unterstützte Sprache lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="dd085-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="dd085-113">Für die Lokalisierung nach dem Buildvorgang können Sie die MUI-Datei kopieren, die sich aus dem Build der ausführbaren Datei und dem Ressourcen Modul ergibt, und die Kopien den Lokalisierern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dd085-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="dd085-114">Im folgenden Verfahren wird davon ausgegangen, dass Win32 PE-Ressourcen mit einem Visual Studio-Projekt für jede Sprache erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="dd085-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="dd085-115">Die grundlegenden Sprachressourcen werden in einer RC-Datei bereitgestellt und mit einem dll-Modul geladen.</span><span class="sxs-lookup"><span data-stu-id="dd085-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="dd085-116">Sie können das Verfahren nach Bedarf wiederholen, um für alle unterstützten Sprachen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd085-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="dd085-117">**So erstellen Sie die Anwendung**</span><span class="sxs-lookup"><span data-stu-id="dd085-117">**To build the application**</span></span>

1.  <span data-ttu-id="dd085-118">Richten Sie ein Visual Studio-Projekt für die Basis Sprache ein.</span><span class="sxs-lookup"><span data-stu-id="dd085-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="dd085-119">Wenn Sie an der Verwendung einer Ressourcen Konfigurationsdatei mit den Ressourcen Tools interessiert sind, legen Sie eine fest, wie unter [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd085-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="dd085-120">Legen Sie Parameter fest, die für das RC-Compilerdienstprogramm in den Eigenschaften Seiten für das Projekt unter **Konfigurations Eigenschaften → Ressourcen → Befehlszeile → zusätzliche Optionen** erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dd085-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="dd085-121">Ausführen des RC-Compilers.</span><span class="sxs-lookup"><span data-stu-id="dd085-121">Run RC Compiler.</span></span> <span data-ttu-id="dd085-122">Das Hilfsprogramm kompiliert und teilt die nicht lokalisierbaren und lokalisierbaren Ressourcen mithilfe von Ressourcen Konfigurationsdaten in zwei verschiedene Objektdateien.</span><span class="sxs-lookup"><span data-stu-id="dd085-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="dd085-123">In diesem Schritt werden die sprach neutralen Ressourcen mit einer LN-Datei verknüpft.</span><span class="sxs-lookup"><span data-stu-id="dd085-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="dd085-124">Weitere Informationen finden Sie in der Beschreibung des Hilfsprogramms unter [Ressourcen Hilfsprogramme](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="dd085-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="dd085-125">Um die sprachspezifischen Ressourcen mit einer sprachspezifischen MUI-Datei zu verknüpfen, legen Sie ein Postbuildereignis für das Projekt auf den Eigenschaften Seiten unter **Konfigurations Eigenschaften → Buildereignisse → Postbuildereignis → Befehlszeile** fest.</span><span class="sxs-lookup"><span data-stu-id="dd085-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="dd085-126">Legen Sie ein Postbuildereignis fest, um den Prüfsummen Wert aus der LN-Datei auf die MUI-Datei für die Sprache anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="dd085-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="dd085-127">Sie können das Dienstprogramm muject für diesen Schritt verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd085-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="dd085-128">Weitere Informationen finden Sie in der Beschreibung des Hilfsprogramms unter [Ressourcen Hilfsprogramme](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="dd085-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="dd085-129">Verwenden Sie die Befehlszeile Postbuildereignis, um Befehle zum Kopieren der Dateien in die entsprechende releaseordnerstruktur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd085-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd085-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd085-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd085-131">Verwenden der mehrsprachigen Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="dd085-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="dd085-132">Vorbereiten einer Ressourcen Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="dd085-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="dd085-133">Ressourcen Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="dd085-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



