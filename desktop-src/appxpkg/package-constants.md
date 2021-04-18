---
title: Paket Konstanten (appmodel. h)
description: Gibt an, wie Pakete verarbeitet werden sollen.
ms.assetid: 72E565C3-6CFD-47E3-8BAC-17D6E86B99DA
topic_type:
- apiref
api_name:
- PACKAGE_APPLICATIONS_MAX_COUNT
- PACKAGE_APPLICATIONS_MIN_COUNT
- PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES
- PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES
- PACKAGE_FILTER_ALL_LOADED
- PACKAGE_FILTER_BUNDLE
- PACKAGE_FILTER_DIRECT
- PACKAGE_FILTER_HEAD
- PACKAGE_FILTER_OPTIONAL
- PACKAGE_FILTER_RESOURCE
- PACKAGE_GRAPH_MAX_SIZE
- PACKAGE_GRAPH_MIN_SIZE
- PACKAGE_INFORMATION_BASIC
- PACKAGE_INFORMATION_FULL
- PACKAGE_MAX_DEPENDENCIES
- PACKAGE_MIN_DEPENDENCIES
- PACKAGE_PROPERTY_BUNDLE
- PACKAGE_PROPERTY_DEVELOPMENT_MODE
- PACKAGE_PROPERTY_FRAMEWORK
- PACKAGE_PROPERTY_OPTIONAL
- PACKAGE_PROPERTY_RESOURCE
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb3a4630eb6e132c7a82ea6b45839f6d2684cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340317"
---
# <a name="package-constants"></a><span data-ttu-id="93483-103">Paket Konstanten</span><span class="sxs-lookup"><span data-stu-id="93483-103">Package constants</span></span>

<span data-ttu-id="93483-104">Gibt an, wie Pakete verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="93483-104">Specifies how packages are to be processed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="93483-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="93483-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="93483-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93483-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MAX_COUNT"></span><span id="package_applications_max_count"></span><dl> <span data-ttu-id="93483-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-108">Die maximale Anzahl von apps in einem Paket.</span><span class="sxs-lookup"><span data-stu-id="93483-108">The maximum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MIN_COUNT"></span><span id="package_applications_min_count"></span><dl> <span data-ttu-id="93483-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-110">Die Mindestanzahl von apps in einem Paket.</span><span class="sxs-lookup"><span data-stu-id="93483-110">The minimum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES"></span><span id="package_family_max_resource_packages"></span><dl> <span data-ttu-id="93483-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-112">Die maximal zulässige Anzahl von Ressourcen Paketen für ein Paket.</span><span class="sxs-lookup"><span data-stu-id="93483-112">The maximum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES"></span><span id="package_family_min_resource_packages"></span><dl> <span data-ttu-id="93483-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-114">Die Mindestanzahl von Ressourcen Paketen, die ein Paket enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="93483-114">The minimum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_ALL_LOADED"></span><span id="package_filter_all_loaded"></span><dl> <span data-ttu-id="93483-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-116">Verarbeiten Sie alle Pakete im Abhängigkeits Diagramm.</span><span class="sxs-lookup"><span data-stu-id="93483-116">Process all packages in the dependency graph.</span></span><br/> <span data-ttu-id="93483-117">Dies entspricht <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.</span><span class="sxs-lookup"><span data-stu-id="93483-117">This is equivalent to <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span><br/>
<blockquote>
[!Note]<br /><span data-ttu-id="93483-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> können nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="93483-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="93483-119">Verwenden Sie stattdessen <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.</span><span class="sxs-lookup"><span data-stu-id="93483-119">Instead, use <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_BUNDLE"></span><span id="package_filter_bundle"></span><dl> <span data-ttu-id="93483-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-121">Verarbeiten von Paket Paketen im Paket Diagramm.</span><span class="sxs-lookup"><span data-stu-id="93483-121">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_DIRECT"></span><span id="package_filter_direct"></span><dl> <span data-ttu-id="93483-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-123">Verarbeiten Sie die direkt abhängigen Pakete des Head (First)-Pakets im Abhängigkeits Diagramm.</span><span class="sxs-lookup"><span data-stu-id="93483-123">Process the directly dependent packages of the head (first) package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_HEAD"></span><span id="package_filter_head"></span><dl> <span data-ttu-id="93483-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-125">Verarbeiten Sie das erste Paket im Abhängigkeits Diagramm.</span><span class="sxs-lookup"><span data-stu-id="93483-125">Process the first package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_OPTIONAL"></span><span id="package_filter_optional"></span><dl> <span data-ttu-id="93483-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-127">Verarbeiten von Paket Paketen im Paket Diagramm.</span><span class="sxs-lookup"><span data-stu-id="93483-127">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_RESOURCE"></span><span id="package_filter_resource"></span><dl> <span data-ttu-id="93483-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-129">Verarbeiten von Ressourcen Paketen im Paket Diagramm.</span><span class="sxs-lookup"><span data-stu-id="93483-129">Process resource packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MAX_SIZE"></span><span id="package_graph_max_size"></span><dl> <span data-ttu-id="93483-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-131">Die maximale Größe eines Paket Diagramms.</span><span class="sxs-lookup"><span data-stu-id="93483-131">The maximum size of a package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MIN_SIZE"></span><span id="package_graph_min_size"></span><dl> <span data-ttu-id="93483-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-133">Die minimale Größe eines Paket Diagramms.</span><span class="sxs-lookup"><span data-stu-id="93483-133">The minimum size of a package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_BASIC"></span><span id="package_information_basic"></span><dl> <span data-ttu-id="93483-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-135">Rufen Sie grundlegende Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="93483-135">Retrieve basic information.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_FULL"></span><span id="package_information_full"></span><dl> <span data-ttu-id="93483-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-137">Abrufen von vollständigen Informationen</span><span class="sxs-lookup"><span data-stu-id="93483-137">Retrieve full information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_MAX_DEPENDENCIES"></span><span id="package_max_dependencies"></span><dl> <span data-ttu-id="93483-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-139">Die maximale Anzahl von Paketen, von denen ein Paket abhängt.</span><span class="sxs-lookup"><span data-stu-id="93483-139">The maximum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_MIN_DEPENDENCIES"></span><span id="package_min_dependencies"></span><dl> <span data-ttu-id="93483-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-141">Die Mindestanzahl von Paketen, von denen ein Paket abhängt.</span><span class="sxs-lookup"><span data-stu-id="93483-141">The minimum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_BUNDLE"></span><span id="package_property_bundle"></span><dl> <span data-ttu-id="93483-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-143">Das Paket ist ein Bündel Paket.</span><span class="sxs-lookup"><span data-stu-id="93483-143">The package is a bundle package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_DEVELOPMENT_MODE"></span><span id="package_property_development_mode"></span><dl> <span data-ttu-id="93483-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000 bis</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-145">Das Paket wurde mit der <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>deploymentoptions</strong></a> -Enumeration registriert.</span><span class="sxs-lookup"><span data-stu-id="93483-145">The package was registered with the <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>DeploymentOptions</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_FRAMEWORK"></span><span id="package_property_framework"></span><dl> <span data-ttu-id="93483-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-147">Das Paket ist ein Framework.</span><span class="sxs-lookup"><span data-stu-id="93483-147">The package is a framework.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_OPTIONAL"></span><span id="package_property_optional"></span><dl> <span data-ttu-id="93483-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-149">Das Paket ist ein optionales Paket.</span><span class="sxs-lookup"><span data-stu-id="93483-149">The package is an optional package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_RESOURCE"></span><span id="package_property_resource"></span><dl> <span data-ttu-id="93483-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="93483-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="93483-151">Das Paket ist ein Ressourcenpaket.</span><span class="sxs-lookup"><span data-stu-id="93483-151">The package is a resource package.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="93483-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93483-152">Requirements</span></span>



| <span data-ttu-id="93483-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93483-153">Requirement</span></span> | <span data-ttu-id="93483-154">Wert</span><span class="sxs-lookup"><span data-stu-id="93483-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93483-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93483-155">Minimum supported client</span></span><br/> | <span data-ttu-id="93483-156">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93483-156">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="93483-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93483-157">Minimum supported server</span></span><br/> | <span data-ttu-id="93483-158">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93483-158">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93483-159">Header</span><span class="sxs-lookup"><span data-stu-id="93483-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="93483-160"><dt>Appmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="93483-160"><dt>AppModel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93483-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93483-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93483-162">**Getcurrentpackageingefo**</span><span class="sxs-lookup"><span data-stu-id="93483-162">**GetCurrentPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)
</dt> <dt>

[<span data-ttu-id="93483-163">**Getpackageingefo**</span><span class="sxs-lookup"><span data-stu-id="93483-163">**GetPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)
</dt> <dt>

[<span data-ttu-id="93483-164">**Packageidfromfullname**</span><span class="sxs-lookup"><span data-stu-id="93483-164">**PackageIdFromFullName**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)
</dt> </dl>

 

