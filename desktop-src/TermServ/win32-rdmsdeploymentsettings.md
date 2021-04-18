---
title: Win32_RDMSDeploymentSettings-Klasse
description: Verwaltet die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste
- Win32_RDMSDeploymentSettings Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517624"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5b8bc-105">Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="5b8bc-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5b8bc-106">Verwaltet die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="5b8bc-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b8bc-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="5b8bc-109">Member</span><span class="sxs-lookup"><span data-stu-id="5b8bc-109">Members</span></span>

<span data-ttu-id="5b8bc-110">Die **Win32 \_ rdmsdeploymentsettings** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5b8bc-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5b8bc-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="5b8bc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5b8bc-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5b8bc-112">Methods</span></span>

<span data-ttu-id="5b8bc-113">Die **Win32 \_ rdmsdeploymentsettings** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="5b8bc-114">Methode</span><span class="sxs-lookup"><span data-stu-id="5b8bc-114">Method</span></span>                                                                                                  | <span data-ttu-id="5b8bc-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b8bc-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b8bc-116">**Getbasevhdpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5b8bc-117">Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="5b8bc-118">**GetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="5b8bc-119">Ruft die Datenbank-Verbindungs Zeichenfolge auf Bereitstellungs Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="5b8bc-120">**Getdiffvhdpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5b8bc-121">Ruft den Verzeichnispfad ab, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="5b8bc-122">**Getexportpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="5b8bc-123">Ruft den Verzeichnispfad ab, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="5b8bc-124">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="5b8bc-125">Ruft eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="5b8bc-126">**Getsecondaryconnectionstring**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="5b8bc-127">Ruft die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene ab, die zur Unterstützung des Kenn Wort Ablaufs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="5b8bc-128">**Getsmbpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="5b8bc-129">Ruft den UNC-Pfad zur SMB-Freigabe ab, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="5b8bc-130">**Getstringarraydeploymentsetting**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="5b8bc-131">Ruft die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="5b8bc-132">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="5b8bc-133">Ruft eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="5b8bc-134">**Removedeploymentsetting**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="5b8bc-135">Löscht die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="5b8bc-136">**Setbasevhdpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5b8bc-137">Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="5b8bc-138">**SetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="5b8bc-139">Legt die Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene fest.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="5b8bc-140">**Setdiffvhdpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="5b8bc-141">Aktualisiert den Verzeichnispfad, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="5b8bc-142">**"Stexportpath"**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="5b8bc-143">Aktualisiert den Verzeichnispfad, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="5b8bc-144">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="5b8bc-145">Aktualisiert eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="5b8bc-146">**Setsecondaryconnectionstring**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="5b8bc-147">Legt die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene fest.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="5b8bc-148">**Setsmbpath**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="5b8bc-149">Aktualisiert den UNC-Pfad zur SMB-Freigabe, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="5b8bc-150">**Setstringarraydeploymentsetting**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="5b8bc-151">Aktualisiert die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="5b8bc-152">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="5b8bc-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="5b8bc-153">Aktualisiert eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5b8bc-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="5b8bc-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b8bc-154">Requirements</span></span>



| <span data-ttu-id="5b8bc-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b8bc-155">Requirement</span></span> | <span data-ttu-id="5b8bc-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5b8bc-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b8bc-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b8bc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5b8bc-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5b8bc-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5b8bc-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b8bc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5b8bc-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b8bc-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5b8bc-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b8bc-161">Namespace</span></span><br/>                | <span data-ttu-id="5b8bc-162">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="5b8bc-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5b8bc-163">MOF</span><span class="sxs-lookup"><span data-stu-id="5b8bc-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b8bc-164"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5b8bc-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b8bc-165">DLL</span><span class="sxs-lookup"><span data-stu-id="5b8bc-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b8bc-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b8bc-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5b8bc-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b8bc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8bc-168">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="5b8bc-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





