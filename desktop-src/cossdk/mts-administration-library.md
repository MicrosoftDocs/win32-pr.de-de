---
description: Die in den com+-Verwaltungs Schnittstellen enthaltene MTS-Verwaltungs Bibliothek bietet Abwärtskompatibilität mit der MTS 2,0-Verwaltungs Bibliothek.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: MTS-Verwaltungs Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523539"
---
# <a name="mts-administration-library"></a><span data-ttu-id="34686-103">MTS-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34686-103">MTS Administration Library</span></span>

<span data-ttu-id="34686-104">Die in den com+-Verwaltungs Schnittstellen enthaltene MTS-Verwaltungs Bibliothek bietet Abwärtskompatibilität mit der MTS 2,0-Verwaltungs Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="34686-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="34686-105">Der größte vorhandene MTS 2,0-Verwaltungs Code funktioniert weiterhin mit der bereitgestellten msadmin-Bibliothek. Allerdings haben sich einige Funktionen geändert.</span><span class="sxs-lookup"><span data-stu-id="34686-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="34686-106">Um die neuen Funktionen nutzen zu können, oder wenn Sie zum ersten Mal Verwaltungs Code schreiben, sollten Sie die COMAdmin-Bibliothek verwenden.</span><span class="sxs-lookup"><span data-stu-id="34686-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="34686-107">Die folgenden Elemente in der aktuellen MTS-Verwaltungs Bibliothek werden in der Bibliothek "MTS 2,0-Verwaltung" geändert:</span><span class="sxs-lookup"><span data-stu-id="34686-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="34686-108">Die **iremotecomponentutil** -Schnittstelle ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34686-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="34686-109">Die **RemoteComponents** -Sammlung ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34686-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="34686-110">Die RoleID-Eigenschaft ist nicht mehr verfügbar. der Rollen Name wird jetzt als Schlüssel für dieses verwendet.</span><span class="sxs-lookup"><span data-stu-id="34686-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="34686-111">Die **exportpackage** -Methode exportiert keine client.exe mehr.</span><span class="sxs-lookup"><span data-stu-id="34686-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="34686-112">Die remotecomponentinstallpath-Eigenschaft wird nicht mehr in der [**LocalComputer**](localcomputer.md) -Sammlung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="34686-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="34686-113">Die applicationinstallpath-Eigenschaft wird nicht mehr in der [**LocalComputer**](localcomputer.md) -Sammlung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="34686-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="34686-114">Das System Paket heißt jetzt Systemanwendung.</span><span class="sxs-lookup"><span data-stu-id="34686-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="34686-115">Das Hilfsprogrammpaket heißt jetzt com+-Hilfsprogramme.</span><span class="sxs-lookup"><span data-stu-id="34686-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="34686-116">Die IsSystem-Eigenschaft ist in der [**Components**](components.md) -Auflistung in mtadmin vorhanden, gibt jedoch "notimpl" zurück, wenn Sie aktiviert ist, und wird nicht gespeichert, wenn Sie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="34686-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="34686-117">Die PackageName-Eigenschaft wird von der [**Components**](components.md) -Auflistung nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34686-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="34686-118">Zum Ermitteln des Paket namens müssen Sie nun die PackageID abrufen und dann das entsprechende Paket in der Paket Auflistung suchen.</span><span class="sxs-lookup"><span data-stu-id="34686-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="34686-119">Die folgenden Eigenschaften sind in der [**interfakesforcomponent**](interfacesforcomponent.md) -Sammlung nicht mehr vorhanden:</span><span class="sxs-lookup"><span data-stu-id="34686-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="34686-120">**Proxyclsid**</span><span class="sxs-lookup"><span data-stu-id="34686-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="34686-121">**Proxydll**</span><span class="sxs-lookup"><span data-stu-id="34686-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="34686-122">**Proxythreadingmodel**</span><span class="sxs-lookup"><span data-stu-id="34686-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="34686-123">**TypeLibFile**</span><span class="sxs-lookup"><span data-stu-id="34686-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="34686-124">**TypeLibID**</span><span class="sxs-lookup"><span data-stu-id="34686-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="34686-125">**Typeliblangid**</span><span class="sxs-lookup"><span data-stu-id="34686-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="34686-126">**Typelibplatform**</span><span class="sxs-lookup"><span data-stu-id="34686-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="34686-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="34686-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="34686-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34686-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34686-129">Automatische Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="34686-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="34686-130">Ergebnisse und Probleme bei der com+-Konvertierung</span><span class="sxs-lookup"><span data-stu-id="34686-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="34686-131">Manuelle Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="34686-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



