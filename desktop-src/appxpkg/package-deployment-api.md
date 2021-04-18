---
title: Paketbereitstellungs-API
description: Erfahren Sie mehr über die paketbereitstellungs-API, die Sie zum Installieren, aktualisieren und Deinstallieren von App-Paketen im System verwenden können. Jedes app-Paket enthält die Dateien, die eine Windows-App bilden, und eine Manifest-Datei, in der die Software für Windows beschrieben wird.
ms.assetid: E2D408E1-6048-4D15-8BF4-69FF6ACF7BD2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a7559739d721781101fad804ebb040333c71c9
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106339053"
---
# <a name="package-deployment-api"></a><span data-ttu-id="4aa7e-104">Paketbereitstellungs-API</span><span class="sxs-lookup"><span data-stu-id="4aa7e-104">Package deployment API</span></span>

<span data-ttu-id="4aa7e-105">Erfahren Sie mehr über die paketbereitstellungs-API, die Sie zum Installieren, aktualisieren und Deinstallieren von App-Paketen im System verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-105">Learn about the package deployment API, which you can use to install, update, and uninstall app packages on the system.</span></span> <span data-ttu-id="4aa7e-106">Jedes app-Paket enthält die Dateien, die eine Windows-App bilden, und eine Manifest-Datei, in der die Software für Windows beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="4aa7e-106">Each app package contains the files that constitute a Windows app, and a manifest file that describes the software to Windows.</span></span>

## <a name="windows-runtime-reference"></a><span data-ttu-id="4aa7e-107">Windows-Runtime-Referenz</span><span class="sxs-lookup"><span data-stu-id="4aa7e-107">Windows Runtime reference</span></span>

-   [<span data-ttu-id="4aa7e-108">**Windows.Management.Deployment**</span><span class="sxs-lookup"><span data-stu-id="4aa7e-108">**Windows.Management.Deployment**</span></span>](/uwp/api/Windows.Management.Deployment)

## <a name="related-topics"></a><span data-ttu-id="4aa7e-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4aa7e-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4aa7e-110">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="4aa7e-110">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="4aa7e-111">Beispiel zum Hinzufügen eines App-Pakets (AddPackage)</span><span class="sxs-lookup"><span data-stu-id="4aa7e-111">Add app package sample (AddPackage)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerAddPackage)
</dt> <dt>

[<span data-ttu-id="4aa7e-112">Beispiel zum Aufzählen von App-Paketen (findpackages)</span><span class="sxs-lookup"><span data-stu-id="4aa7e-112">Enumerate app packages sample (FindPackages)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerFindPackages)
</dt> <dt>

[<span data-ttu-id="4aa7e-113">Beispiel für das Auflisten von App-Paketen nach Name und Herausgeber (findpackagesbynameandpublisher)</span><span class="sxs-lookup"><span data-stu-id="4aa7e-113">Enumerate app packages by name and publisher sample (FindPackagesByNameAndPublisher)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerFindPackagesByNameAndPublisher)
</dt> <dt>

[<span data-ttu-id="4aa7e-114">Beispiel für das Auflisten von App-Paketen nach Benutzer-sid (findpackagesbyusersecurityid)</span><span class="sxs-lookup"><span data-stu-id="4aa7e-114">Enumerate app packages by user SID sample (FindPackagesByUserSecurityId)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerFindPackagesByUserSecurityIda)
</dt> <dt>

[<span data-ttu-id="4aa7e-115">Beispiel zum Entfernen eines App-Pakets (RemovePackage)</span><span class="sxs-lookup"><span data-stu-id="4aa7e-115">Remove app package sample (RemovePackage)</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PackageManagerRemovePackage)
</dt> <dt>

<span data-ttu-id="4aa7e-116">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="4aa7e-116">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="4aa7e-117">[App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="4aa7e-117">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="4aa7e-118">Glossar</span><span class="sxs-lookup"><span data-stu-id="4aa7e-118">Glossary</span></span>](appx-packaging-glossary.md)
</dt> <dt>

<span data-ttu-id="4aa7e-119">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4aa7e-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4aa7e-120">App-Paketmanifestschema</span><span class="sxs-lookup"><span data-stu-id="4aa7e-120">App package manifest schema</span></span>](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[<span data-ttu-id="4aa7e-121">Verpacken von APIs</span><span class="sxs-lookup"><span data-stu-id="4aa7e-121">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="4aa7e-122">Paket Abfrage-API</span><span class="sxs-lookup"><span data-stu-id="4aa7e-122">Package query API</span></span>](functions.md)
</dt> </dl>

 

 