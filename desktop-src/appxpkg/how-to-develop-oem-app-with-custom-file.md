---
title: So entwickeln Sie eine OEM-APP, die eine benutzerdefinierte Datei verwendet
description: Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die APP zu übergeben.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106339474"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="c1e08-103">So entwickeln Sie eine OEM-APP, die eine benutzerdefinierte Datei verwendet</span><span class="sxs-lookup"><span data-stu-id="c1e08-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="c1e08-104">Weitere Informationen zum Erstellen und Verwenden von benutzerdefinierten Datendateien finden Sie unter [(. AppX-oder appxbundle)-Wartungs Command-Line Optionen](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span><span class="sxs-lookup"><span data-stu-id="c1e08-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="c1e08-105">Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die APP zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c1e08-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="c1e08-106">Für apps, die Sie für die OEM-Bereitstellung erstellen, können Sie eine benutzerdefinierte Datei verwenden, um Informationen vom OEM an die apps zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c1e08-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="c1e08-107">Um OEM-Informationen an eine APP zu übergeben, erstellen Sie eine benutzerdefinierte Datendatei im Ordner microsoft.system. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="c1e08-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="c1e08-108">Der Dateiname ist für das betriebssystemspezifisch und wird bei Betriebssystemupdates automatisch weitergeführt.</span><span class="sxs-lookup"><span data-stu-id="c1e08-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="c1e08-109">OEMs können diese Datei verwenden, um benutzerdefinierte Bezeichner zu übergeben, damit apps wissen, wann Sie von OEMs bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c1e08-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="c1e08-110">Sie können nur eine benutzerdefinierte Datendatei pro APP haben.</span><span class="sxs-lookup"><span data-stu-id="c1e08-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="c1e08-111">Apps müssen in der Lage sein, diese Datei ordnungsgemäß zu suchen und zu lesen.</span><span class="sxs-lookup"><span data-stu-id="c1e08-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="c1e08-112">Entwickler behandeln die Datei als nicht vertrauenswürdige Daten.</span><span class="sxs-lookup"><span data-stu-id="c1e08-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c1e08-113">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="c1e08-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c1e08-114">Technologien</span><span class="sxs-lookup"><span data-stu-id="c1e08-114">Technologies</span></span>

-   [<span data-ttu-id="c1e08-115">Schnellstart: Abfragen von Informationen zum App-Paket Manifest</span><span class="sxs-lookup"><span data-stu-id="c1e08-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="c1e08-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c1e08-116">Prerequisites</span></span>

-   <span data-ttu-id="c1e08-117">Sie benötigen das Tool zur [Abbild Verwaltung für die Bereitstellung (Mage)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , um das App-Paket mit der benutzerdefinierten Datendatei hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1e08-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="c1e08-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="c1e08-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="c1e08-119">Schritt 1: Erstellen Sie eine benutzerdefinierte Datei und fügen Sie Sie dem paketmetadatenordner hinzu</span><span class="sxs-lookup"><span data-stu-id="c1e08-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="c1e08-120">Sie können Ihre APP so entwerfen, dass Sie ein beliebiges Format verwendet, das Sie für benutzerdefinierte Daten auswählen.</span><span class="sxs-lookup"><span data-stu-id="c1e08-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="c1e08-121">Beispielsweise können Sie XML, eine Textdatei oder einen anderen Dateityp verwenden, um Ihre Daten zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="c1e08-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="c1e08-122">Es wird empfohlen, zu überprüfen, wie Sie die Datei testen und validieren können.</span><span class="sxs-lookup"><span data-stu-id="c1e08-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="c1e08-123">Beispielsweise können Sie ein XML-Schema erstellen, um eine XML-Datei zu validieren.</span><span class="sxs-lookup"><span data-stu-id="c1e08-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="c1e08-124">Sie können einen beliebigen Dateityp mit einem beliebigen Dateinamen für die benutzerdefinierten Daten angeben.</span><span class="sxs-lookup"><span data-stu-id="c1e08-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="c1e08-125">Wenn Sie das App-Paket mit der benutzerdefinierten Datendatei mithilfe des [Tools zum](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) renderingtool hinzufügen, benennt das-Objekt die benutzerdefinierte Datei in "Custom. Data" um und speichert die Datei im Ordner "microsoft.system. Package. Metadata".</span><span class="sxs-lookup"><span data-stu-id="c1e08-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="c1e08-126">Die benutzerdefinierte Datendatei kann nicht von der APP geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c1e08-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="c1e08-127">Es handelt sich um eine schreibgeschützte Ressource.</span><span class="sxs-lookup"><span data-stu-id="c1e08-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="c1e08-128">Schritt 2: Zugreifen auf die benutzerdefinierte Datendatei für eine APP</span><span class="sxs-lookup"><span data-stu-id="c1e08-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="c1e08-129">Sie können auf die benutzerdefinierte. Data-Datei für eine APP aus Ihrem Code zugreifen, indem Sie Windows-APIs verwenden, um Informationen für das aktuelle Paket zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1e08-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="c1e08-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c1e08-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="c1e08-131">Weitere Informationen zum Entwickeln mit der " [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) "-Eigenschaft finden Sie unter [Schnellstart: Abfragen von App-Paket Manifest-Informationen](how-to-query-package-identity-information.md).</span><span class="sxs-lookup"><span data-stu-id="c1e08-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="c1e08-132">Weitere Informationen über den Zugriff auf die benutzerdefinierte Datendatei über [**istoragefolder. getfileasync**](/uwp/api/windows.storage.istoragefolder.getfileasync) und die Verwendung von [**storagefile**](/uwp/api/Windows.Storage.StorageFile) -Objekten finden Sie unter [zugreifen auf Daten und Dateien](/previous-versions/windows/apps/hh464959(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="c1e08-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1e08-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1e08-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1e08-134">Schnellstart: Abfragen von Informationen zum App-Paket Manifest</span><span class="sxs-lookup"><span data-stu-id="c1e08-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 