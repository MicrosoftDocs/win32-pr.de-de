---
title: Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden
description: Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Device Manager, IDL-Dateien
- Device Manager, IDL-Dateien
- Desktop Anwendungen, IDL-Dateien
- Dienstanbieter, IDL-Dateien
- Programmier Handbuch, IDL-Dateien
- IDL-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337998"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="c9244-109">Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="c9244-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="c9244-110">Das Windows Media Device Manager SDK umfasst sowohl Header Dateien als auch die Quell-IDL-Dateien für die meisten dieser Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="c9244-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="c9244-111">Die Header Dateien befinden sich im \\ Ordner "Inc" \\ im SDK-Installationspfad.</span><span class="sxs-lookup"><span data-stu-id="c9244-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="c9244-112">Die IDL-Dateien befinden sich im \\ IDL- \\ Ordner.</span><span class="sxs-lookup"><span data-stu-id="c9244-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="c9244-113">Die vorkompilierten Header sind viel einfacher zu verwenden, und mehrere der IDL-Dateien werden zu einem einzelnen bereitgestellten Header zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="c9244-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="c9244-114">Wenn Sie jedoch ihre eigenen Header Dateien aus den bereitgestellten IDL-Dateien verarbeiten möchten, wird in diesem Thema beschrieben, welche IDL-Dateien welche Header Dateien erstellen. Außerdem werden die Abhängigkeiten der einzelnen IDL-Dateien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c9244-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="c9244-115">**Äquivalente IDL und bereitgestellte Header Dateien**</span><span class="sxs-lookup"><span data-stu-id="c9244-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="c9244-116">**IDL**</span><span class="sxs-lookup"><span data-stu-id="c9244-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="c9244-117">**Gleichwertig bereitgestellter**</span><span class="sxs-lookup"><span data-stu-id="c9244-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="c9244-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9244-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9244-119">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-119">WMDM.idl</span></span><br/> <span data-ttu-id="c9244-120">Wmsp. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-120">WMSP.idl</span></span><br/> <span data-ttu-id="c9244-121">Wmscp. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-121">WMSCP.idl</span></span><br/> <span data-ttu-id="c9244-122">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="c9244-123">Mtaumdm. h</span><span class="sxs-lookup"><span data-stu-id="c9244-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="c9244-124">Alle vier IDL-Dateien sind in diesem einzelnen bereitgestellten Header enthalten.</span><span class="sxs-lookup"><span data-stu-id="c9244-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="c9244-125">**WMDM. idl** definiert alle Anwendungsschnittstellen und erforderlichen Strukturen, Konstanten und Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="c9244-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="c9244-126">**Wmsp. idl** definiert alle Dienstanbieter Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="c9244-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="c9244-127">**Wmscp. idl** definiert alle Schnittstellen, GUID-Werte und Konstanten, die von sicheren Inhaltsanbietern benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="c9244-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="c9244-128">**icomponentauthenticate. idl** definiert die [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c9244-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="c9244-129">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="c9244-130">Wmdmlog. h</span><span class="sxs-lookup"><span data-stu-id="c9244-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="c9244-131">wmdmlog \_ i. c</span><span class="sxs-lookup"><span data-stu-id="c9244-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="c9244-132">Definiert die Protokollierungs Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="c9244-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="c9244-133">Beide bereitgestellten Header Dateien müssen anstelle der h-Datei verwendet werden, da ein Problem mit der IDL-Datei vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c9244-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="c9244-134">Wmdrmdeviceapp. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="c9244-135">Wmdrmdeviceapp. h</span><span class="sxs-lookup"><span data-stu-id="c9244-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="c9244-136">Definiert die [**iwmdrmdeviceapp**](iwmdrmdeviceapp.md) -und [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) -Schnittstellen, die von Anwendungen verwendet werden, die DRM auf Geräten oder die Anzahl der Wiedergabe Zähler auf Geräten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c9244-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="c9244-137">**IDL-Abhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="c9244-137">**IDL Dependencies**</span></span>

<span data-ttu-id="c9244-138">Einige der bereitgestellten IDL-Dateien haben Buildabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="c9244-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="c9244-139">Wenn Sie beabsichtigen, die IDL-Dateien selbst zu kompilieren, müssen Sie diese externen Abhängigkeiten in der in der folgenden Tabelle gezeigten Reihenfolge verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c9244-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9244-140">**IDL**</span><span class="sxs-lookup"><span data-stu-id="c9244-140">**IDL**</span></span>                    | <span data-ttu-id="c9244-141">**Abhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="c9244-141">**Dependencies**</span></span>                                                                 |
| <span data-ttu-id="c9244-142">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="c9244-143">Importieren Sie "oaidl. idl";</span><span class="sxs-lookup"><span data-stu-id="c9244-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="c9244-144">\#"icomponentauthenticate. idl" einschließen</span><span class="sxs-lookup"><span data-stu-id="c9244-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="c9244-145">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-145">WMDM.idl</span></span>                   | <span data-ttu-id="c9244-146">Keine externen Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="c9244-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="c9244-147">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-147">WmdmLog.idl</span></span>                | <span data-ttu-id="c9244-148">Keine externen Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="c9244-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="c9244-149">Wmdrmdeviceapp. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="c9244-150">Keine externen Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="c9244-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="c9244-151">Wmscp. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-151">WMSCP.idl</span></span>                  | <span data-ttu-id="c9244-152">\#"wmdrmdeviceapp. idl" einschließen</span><span class="sxs-lookup"><span data-stu-id="c9244-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="c9244-153">\#"wmsp. idl" einschließen</span><span class="sxs-lookup"><span data-stu-id="c9244-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="c9244-154">Wmsp. idl</span><span class="sxs-lookup"><span data-stu-id="c9244-154">WMSP.idl</span></span>                   | <span data-ttu-id="c9244-155">\#"WMDM. idl" einschließen</span><span class="sxs-lookup"><span data-stu-id="c9244-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="c9244-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9244-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9244-157">**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="c9244-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





