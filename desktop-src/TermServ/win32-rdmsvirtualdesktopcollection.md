---
title: Win32_RDMSVirtualDesktopCollection-Klasse
description: Erstellt und verwaltet eine Sammlung virtueller Desktops.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste
- Win32_RDMSVirtualDesktopCollection Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341600"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="fa84d-105">Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="fa84d-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="fa84d-106">Erstellt und verwaltet eine Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="fa84d-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="fa84d-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa84d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa84d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa84d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="fa84d-109">Member</span><span class="sxs-lookup"><span data-stu-id="fa84d-109">Members</span></span>

<span data-ttu-id="fa84d-110">Die **Win32 \_ rdmsvirtualdesktopcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fa84d-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="fa84d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa84d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fa84d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa84d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fa84d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa84d-113">Methods</span></span>

<span data-ttu-id="fa84d-114">Die **Win32 \_ rdmsvirtualdesktopcollection** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fa84d-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="fa84d-115">Methode</span><span class="sxs-lookup"><span data-stu-id="fa84d-115">Method</span></span>                                                                                            | <span data-ttu-id="fa84d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa84d-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa84d-117">**Addvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="fa84d-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="fa84d-118">Fügt einer Sammlung virtueller Desktops einen virtuellen Desktop hinzu.</span><span class="sxs-lookup"><span data-stu-id="fa84d-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="fa84d-119">**Cancelpatch**</span><span class="sxs-lookup"><span data-stu-id="fa84d-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="fa84d-120">Bricht einen Bereitstellungs Auftrag für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="fa84d-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="fa84d-121">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="fa84d-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="fa84d-122">Ruft einen ganzzahligen Eigenschafts Wert aus einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="fa84d-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="fa84d-123">**Getpatchproperties**</span><span class="sxs-lookup"><span data-stu-id="fa84d-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="fa84d-124">Ruft die Eigenschaften eines Bereitstellungs Auftrags für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="fa84d-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="fa84d-125">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="fa84d-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="fa84d-126">Ruft einen Zeichen folgen Eigenschafts Wert aus einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="fa84d-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="fa84d-127">**Provisioningenvereratejobs**</span><span class="sxs-lookup"><span data-stu-id="fa84d-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="fa84d-128">Listet die Bereitstellungs Aufträge virtueller Desktops für diesen Dienst auf.</span><span class="sxs-lookup"><span data-stu-id="fa84d-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="fa84d-129">**Provisioningjobcancel**</span><span class="sxs-lookup"><span data-stu-id="fa84d-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="fa84d-130">Bricht einen Bereitstellungs Auftrag für virtuelle Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="fa84d-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="fa84d-131">**Provisioningjobexecute**</span><span class="sxs-lookup"><span data-stu-id="fa84d-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="fa84d-132">Führt einen Bereitstellungs Auftrag für virtuelle Desktops aus.</span><span class="sxs-lookup"><span data-stu-id="fa84d-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="fa84d-133">**Provisioningjobgetreport**</span><span class="sxs-lookup"><span data-stu-id="fa84d-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="fa84d-134">Ruft einen Bericht zum Status eines virtuellen Desktop Bereitstellungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="fa84d-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="fa84d-135">**Provisioningprepjob**</span><span class="sxs-lookup"><span data-stu-id="fa84d-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="fa84d-136">Erstellt einen Bereitstellungs Auftrag für virtuelle Desktops.</span><span class="sxs-lookup"><span data-stu-id="fa84d-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="fa84d-137">**Removevirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="fa84d-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="fa84d-138">Entfernt einen virtuellen Desktop aus einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="fa84d-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="fa84d-139">**Schedulepatch**</span><span class="sxs-lookup"><span data-stu-id="fa84d-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="fa84d-140">Plant einen Bereitstellungs Auftrag für Software Updates, mit dem Software Updates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.</span><span class="sxs-lookup"><span data-stu-id="fa84d-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="fa84d-141">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="fa84d-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="fa84d-142">Aktualisiert einen ganzzahligen Eigenschafts Wert einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="fa84d-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="fa84d-143">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="fa84d-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="fa84d-144">Aktualisiert den Wert einer Zeichen folgen Eigenschaft einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="fa84d-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="fa84d-145">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa84d-145">Properties</span></span>

<span data-ttu-id="fa84d-146">Die **Win32 \_ rdmsvirtualdesktopcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa84d-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa84d-147">**Alias**</span><span class="sxs-lookup"><span data-stu-id="fa84d-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa84d-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-150">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa84d-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-151">Ruft den Alias der Auflistung ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-152">**Collectiondescription**</span><span class="sxs-lookup"><span data-stu-id="fa84d-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa84d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-155">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa84d-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-156">Ruft die Beschreibung der Auflistung ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-157">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="fa84d-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-158">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="fa84d-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-160">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa84d-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-161">Ruft ein Array von-Werten ab, die Symbole für die Auflistung angeben, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-162">**Isha**</span><span class="sxs-lookup"><span data-stu-id="fa84d-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-163">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fa84d-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-165">Ruft einen Wert ab, der angibt, ob die Auflistung hoch verfügbare VMS enthält, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="fa84d-166">**True** , wenn die Sammlung hoch verfügbare VMS enthält. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fa84d-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-167">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="fa84d-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fa84d-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-170">Ruft einen Wert ab, der angibt, ob die Auflistung verwaltet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="fa84d-171">**True** , wenn die Auflistung verwaltet wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fa84d-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-172">**Isuseradmin**</span><span class="sxs-lookup"><span data-stu-id="fa84d-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-173">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fa84d-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-175">Ruft einen Wert ab, der angibt, ob ein Benutzer ein Administrator auf einem virtuellen Computer ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="fa84d-176">**True** , wenn der Benutzer ein Administrator auf einem virtuellen Computer ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fa84d-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="fa84d-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa84d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-180">Ruft den Namen der Auflistung ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-181">**Rollback aktiviert**</span><span class="sxs-lookup"><span data-stu-id="fa84d-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-182">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fa84d-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-183">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-184">Ruft einen Wert ab, der angibt, ob ein virtueller Computer mit einer VM-Momentaufnahme erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa84d-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="fa84d-185">**True** , wenn die VM mit einer VM-Momentaufnahme erstellt wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fa84d-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fa84d-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa84d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-188">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-189">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa84d-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-190">Dient zum Abrufen oder Festlegen einer Sicherheits Beschreibung, die die SSDL-Sicherheit steuert, die den Zugriff auf die Auflistung steuert.</span><span class="sxs-lookup"><span data-stu-id="fa84d-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-191">**Showinportal**</span><span class="sxs-lookup"><span data-stu-id="fa84d-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-192">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fa84d-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-194">Ruft einen Wert ab, der angibt, ob die Auflistung in terminaldiensteWebzugriff (TS Webzugriff) angezeigt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="fa84d-195">**True** zum Anzeigen der Auflistung in TS Webzugriff; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fa84d-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-196">**Type**</span><span class="sxs-lookup"><span data-stu-id="fa84d-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa84d-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-198">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-199">Ruft einen Wert ab, der den Typ der von der Auflistung gehosteten Sitzungen von virtuellen Maschinen angibt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="fa84d-200">Diese Eigenschaft enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="fa84d-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="fa84d-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**Tempvm** (1)</span><span class="sxs-lookup"><span data-stu-id="fa84d-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa84d-202">Temporäre virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="fa84d-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="fa84d-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**Manualpersonalvm** (2)</span><span class="sxs-lookup"><span data-stu-id="fa84d-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa84d-204">Manuell erstellte virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="fa84d-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="fa84d-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**Autopersonalvm** (3)</span><span class="sxs-lookup"><span data-stu-id="fa84d-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa84d-206">Automatisch generierte virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="fa84d-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa84d-207">**Uservhdsetting**</span><span class="sxs-lookup"><span data-stu-id="fa84d-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa84d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-209">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-210">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa84d-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-211">Ruft die Einstellung für die Benutzerdaten-VHD für die Auflistung ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="fa84d-212">**Vmfarmsettings**</span><span class="sxs-lookup"><span data-stu-id="fa84d-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa84d-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa84d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa84d-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa84d-215">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa84d-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa84d-216">Ruft die Desktop Einstellungen für die virtuellen Maschinen in der Auflistung ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fa84d-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa84d-217">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa84d-217">Requirements</span></span>



| <span data-ttu-id="fa84d-218">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa84d-218">Requirement</span></span> | <span data-ttu-id="fa84d-219">Wert</span><span class="sxs-lookup"><span data-stu-id="fa84d-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa84d-220">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa84d-220">Minimum supported client</span></span><br/> | <span data-ttu-id="fa84d-221">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fa84d-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fa84d-222">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa84d-222">Minimum supported server</span></span><br/> | <span data-ttu-id="fa84d-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa84d-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fa84d-224">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa84d-224">Namespace</span></span><br/>                | <span data-ttu-id="fa84d-225">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="fa84d-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fa84d-226">MOF</span><span class="sxs-lookup"><span data-stu-id="fa84d-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa84d-227"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fa84d-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa84d-228">DLL</span><span class="sxs-lookup"><span data-stu-id="fa84d-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa84d-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa84d-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fa84d-230">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa84d-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa84d-231">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="fa84d-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

