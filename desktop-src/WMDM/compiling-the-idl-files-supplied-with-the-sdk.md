---
title: Kompilieren der mit dem SDK bereitgestellten IDL-Dateien
description: Kompilieren der mit dem SDK bereitgestellten IDL-Dateien
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Geräte-Manager,IDL-Dateien
- Geräte-Manager,IDL-Dateien
- Desktopanwendungen, IDL-Dateien
- Dienstanbieter, IDL-Dateien
- Programmierhandbuch, IDL-Dateien
- IDL-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444011"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="f1a3d-109">Kompilieren der mit dem SDK bereitgestellten IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="f1a3d-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="f1a3d-110">Das Windows Media Geräte-Manager SDK enthält sowohl Headerdateien als auch die IDL-Quelldateien für die meisten dieser Headerdateien.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="f1a3d-111">Die Headerdateien befinden sich im \\ Ordner inc \\ im SDK-Installationspfad.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="f1a3d-112">Die IDL-Dateien befinden sich im \\ Ordner \\ idl.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="f1a3d-113">Die vorkompilierten Header sind viel einfacher zu verwenden, und einige der IDL-Dateien werden zu einem einzelnen bereitgestellten Header kombiniert.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="f1a3d-114">Wenn Sie jedoch ihre eigenen Headerdateien aus den bereitgestellten IDL-Dateien verarbeiten möchten, wird in diesem Thema beschrieben, welche IDL-Dateien welche Headerdateien erstellen, und es werden auch die Abhängigkeiten der einzelnen IDL-Dateien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="f1a3d-115">**Äquivalente IDL- und bereitgestellte Headerdateien**</span><span class="sxs-lookup"><span data-stu-id="f1a3d-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="f1a3d-116">**Idl**</span><span class="sxs-lookup"><span data-stu-id="f1a3d-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="f1a3d-117">**Entsprechender angegebener Header**</span><span class="sxs-lookup"><span data-stu-id="f1a3d-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="f1a3d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1a3d-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a3d-119">WMDM.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-119">WMDM.idl</span></span><br/> <span data-ttu-id="f1a3d-120">WMSP.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-120">WMSP.idl</span></span><br/> <span data-ttu-id="f1a3d-121">WMSCP.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-121">WMSCP.idl</span></span><br/> <span data-ttu-id="f1a3d-122">icomponentauthenticate.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="f1a3d-123">Mswmdm.h</span><span class="sxs-lookup"><span data-stu-id="f1a3d-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="f1a3d-124">Alle vier IDL-Dateien sind in diesem einzelnen bereitgestellten Header enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="f1a3d-125">**WMDM.idl** Definiert alle Anwendungsschnittstellen und erforderlichen Strukturen, Konstanten und Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="f1a3d-126">**WMSP.idl** Definiert alle Dienstanbieterschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="f1a3d-127">**WMSCP.idl** Definiert alle Schnittstellen, GUID-Werte und Konstanten, die von sicheren Inhaltsanbietern benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="f1a3d-128">**icomponentauthenticate.idl** Definiert die [**IComponentAuthenticate-Schnittstelle.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)</span><span class="sxs-lookup"><span data-stu-id="f1a3d-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="f1a3d-129">Wmdmlog.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="f1a3d-130">Wmdmlog.h</span><span class="sxs-lookup"><span data-stu-id="f1a3d-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="f1a3d-131">wmdmlog \_ i.c</span><span class="sxs-lookup"><span data-stu-id="f1a3d-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="f1a3d-132">Definiert die Protokollierungsschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="f1a3d-133">Beide angegebenen Headerdateien müssen aufgrund eines Problems mit der IDL-Datei anstelle der H-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f1a3d-134">WMDRMDeviceApp.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="f1a3d-135">Wmdrmdeviceapp.h</span><span class="sxs-lookup"><span data-stu-id="f1a3d-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="f1a3d-136">Definiert die [**IWMDRMDeviceApp-**](iwmdrmdeviceapp.md) und [**IWMDRMDeviceApp2-Schnittstellen,**](iwmdrmdeviceapp2.md) die von Anwendungen verwendet werden, die DRM auf Geräten aktualisieren, oder die Anzahl der Wiedergaben von Zählern auf Geräten.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="f1a3d-137">**IDL-Abhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="f1a3d-137">**IDL Dependencies**</span></span>

<span data-ttu-id="f1a3d-138">Einige der bereitgestellten IDL-Dateien verfügen über Buildabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="f1a3d-139">Wenn Sie die IDL-Dateien selbst kompilieren möchten, müssen Sie diese externen Abhängigkeiten in der in der folgenden Tabelle gezeigten Reihenfolge verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f1a3d-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="f1a3d-140">Idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-140">IDL</span></span>                      |   <span data-ttu-id="f1a3d-141">Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="f1a3d-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1a3d-142">icomponentauthenticate.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="f1a3d-143">import "oaidl.idl";</span><span class="sxs-lookup"><span data-stu-id="f1a3d-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="f1a3d-144">\#include "icomponentauthenticate.idl"</span><span class="sxs-lookup"><span data-stu-id="f1a3d-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="f1a3d-145">WMDM.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-145">WMDM.idl</span></span>                   | <span data-ttu-id="f1a3d-146">Keine externen Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="f1a3d-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="f1a3d-147">WmdmLog.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-147">WmdmLog.idl</span></span>                | <span data-ttu-id="f1a3d-148">Keine externen Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="f1a3d-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="f1a3d-149">WMDRMDeviceApp.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="f1a3d-150">Keine externen Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="f1a3d-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="f1a3d-151">WMSCP.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-151">WMSCP.idl</span></span>                  | <span data-ttu-id="f1a3d-152">\#include "WMDRMDeviceApp.idl"</span><span class="sxs-lookup"><span data-stu-id="f1a3d-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="f1a3d-153">\#include "WMSP.idl"</span><span class="sxs-lookup"><span data-stu-id="f1a3d-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="f1a3d-154">WMSP.idl</span><span class="sxs-lookup"><span data-stu-id="f1a3d-154">WMSP.idl</span></span>                   | <span data-ttu-id="f1a3d-155">\#include "WMDM.idl"</span><span class="sxs-lookup"><span data-stu-id="f1a3d-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="f1a3d-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1a3d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1a3d-157">**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="f1a3d-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





