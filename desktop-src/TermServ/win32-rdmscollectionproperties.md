---
title: Win32_RDMSCollectionProperties-Klasse
description: Verwaltet die Eigenschaften einer Sammlung virtueller Desktops.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties-Klasse Remotedesktopdienste
- Win32_RDMSCollectionProperties Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391807"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="29943-105">Win32 \_ rdmscollectionproperties-Klasse</span><span class="sxs-lookup"><span data-stu-id="29943-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="29943-106">Verwaltet die Eigenschaften einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="29943-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="29943-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29943-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29943-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29943-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="29943-109">Member</span><span class="sxs-lookup"><span data-stu-id="29943-109">Members</span></span>

<span data-ttu-id="29943-110">Die **Win32 \_ rdmscollectionproperties** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="29943-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="29943-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="29943-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="29943-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29943-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="29943-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="29943-113">Methods</span></span>

<span data-ttu-id="29943-114">Die **Win32-Klasse \_ rdmscollectionproperties** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="29943-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="29943-115">Methode</span><span class="sxs-lookup"><span data-stu-id="29943-115">Method</span></span>                                                                                        | <span data-ttu-id="29943-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29943-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="29943-117">**Getprovisioningproperties**</span><span class="sxs-lookup"><span data-stu-id="29943-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="29943-118">Ruft die Bereitstellungs Eigenschaften der Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="29943-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="29943-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29943-119">Properties</span></span>

<span data-ttu-id="29943-120">Die **Win32 \_ rdmscollectionproperties** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29943-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29943-121">**Alias**</span><span class="sxs-lookup"><span data-stu-id="29943-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29943-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29943-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29943-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="29943-125">Ruft den Alias der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="29943-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="29943-126">**Referencevirtualdesktopadapters**</span><span class="sxs-lookup"><span data-stu-id="29943-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-127">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="29943-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29943-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-129">Ruft die Namen der virtuellen Netzwerkadapter der Master-VM ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="29943-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-130">**Referencevirtualdesktoparchitecture**</span><span class="sxs-lookup"><span data-stu-id="29943-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-133">Ruft die Prozessorarchitektur der Master-VM ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="29943-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-134">**Referencevirtualdesktopguid**</span><span class="sxs-lookup"><span data-stu-id="29943-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-137">Ruft die GUID der Master-VM ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="29943-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-138">**Referencevirtualdesktophost**</span><span class="sxs-lookup"><span data-stu-id="29943-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-141">Ruft den Namen des Host Servers der Master-VM ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="29943-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-142">**Referencevirtualdesktopmachinename**</span><span class="sxs-lookup"><span data-stu-id="29943-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-145">Ruft den Computernamen der Master-VM ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="29943-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-146">**Referencevirtualdesktopname**</span><span class="sxs-lookup"><span data-stu-id="29943-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-149">Ruft den Namen der Master-VM ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="29943-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-150">**Referencevirtualdesktoposversion**</span><span class="sxs-lookup"><span data-stu-id="29943-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29943-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29943-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-153">Ruft die Betriebssystemversion der Master-VM ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="29943-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-154">**Referencevirtualdesktopramsizemb**</span><span class="sxs-lookup"><span data-stu-id="29943-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29943-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29943-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-157">Ruft die Arbeitsspeicher Größe der Master-VM ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="29943-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="29943-158">**Referencevirtualdesktopremotefx**</span><span class="sxs-lookup"><span data-stu-id="29943-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29943-159">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="29943-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29943-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29943-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29943-161">Ruft einen Wert ab, der angibt, ob remotefx für die Master-VM aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="29943-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="29943-162">**True** , wenn remotefx aktiviert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="29943-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="29943-163">Der Standardwert für diese Eigenschaft ist **false**.</span><span class="sxs-lookup"><span data-stu-id="29943-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29943-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29943-164">Requirements</span></span>



| <span data-ttu-id="29943-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29943-165">Requirement</span></span> | <span data-ttu-id="29943-166">Wert</span><span class="sxs-lookup"><span data-stu-id="29943-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="29943-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29943-167">Minimum supported client</span></span><br/> | <span data-ttu-id="29943-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="29943-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="29943-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29943-169">Minimum supported server</span></span><br/> | <span data-ttu-id="29943-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29943-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="29943-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="29943-171">Namespace</span></span><br/>                | <span data-ttu-id="29943-172">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="29943-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="29943-173">MOF</span><span class="sxs-lookup"><span data-stu-id="29943-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29943-174"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="29943-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="29943-175">DLL</span><span class="sxs-lookup"><span data-stu-id="29943-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29943-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29943-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="29943-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29943-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29943-178">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="29943-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

