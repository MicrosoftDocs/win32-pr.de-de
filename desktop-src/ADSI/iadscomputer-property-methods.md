---
title: Iadscomputer-Eigenschaften Methoden (IADs. h)
description: Die iadscomputer-Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Iadscomputer-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859116"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="e7e59-105">Iadscomputer-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="e7e59-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="e7e59-106">Die [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) -Schnittstellen Methoden lesen und schreiben die in diesem Thema beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e7e59-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="e7e59-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="e7e59-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e7e59-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7e59-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="e7e59-109">**Computer-ID**</span><span class="sxs-lookup"><span data-stu-id="e7e59-109">**ComputerID**</span></span>
<span data-ttu-id="e7e59-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-111">Die den einzelnen Computern zugewiesenen Globally Unique Identifier.</span><span class="sxs-lookup"><span data-stu-id="e7e59-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="e7e59-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7e59-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-114">**Abteilung**</span><span class="sxs-lookup"><span data-stu-id="e7e59-114">**Department**</span></span>
<span data-ttu-id="e7e59-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-116">Die Organisationseinheit (OU), z. b. die Abteilung, zu der dieser Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="e7e59-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="e7e59-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7e59-119">**Description**</span></span>
<span data-ttu-id="e7e59-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-121">Die Beschreibung dieses Computers.</span><span class="sxs-lookup"><span data-stu-id="e7e59-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-124">**Division**</span><span class="sxs-lookup"><span data-stu-id="e7e59-124">**Division**</span></span>
<span data-ttu-id="e7e59-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-126">Die Division innerhalb einer Organisation, der dieser Computer angehört.</span><span class="sxs-lookup"><span data-stu-id="e7e59-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="e7e59-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-129">**Location**</span><span class="sxs-lookup"><span data-stu-id="e7e59-129">**Location**</span></span>
<span data-ttu-id="e7e59-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-131">Der zugewiesene physische Speicherort dieses Computers.</span><span class="sxs-lookup"><span data-stu-id="e7e59-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-133">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-134">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="e7e59-134">**MemorySize**</span></span>
<span data-ttu-id="e7e59-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-136">Die Größe des zufälligen zugriffsspeichers für diesen Computer in Megabyte.</span><span class="sxs-lookup"><span data-stu-id="e7e59-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-138">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-139">**Modell**</span><span class="sxs-lookup"><span data-stu-id="e7e59-139">**Model**</span></span>
<span data-ttu-id="e7e59-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-141">Die Marke und das Modell dieses Computers.</span><span class="sxs-lookup"><span data-stu-id="e7e59-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-143">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-144">**Netzwerkadressen**</span><span class="sxs-lookup"><span data-stu-id="e7e59-144">**NetAddresses**</span></span>
<span data-ttu-id="e7e59-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-146">Ein Array von netaddress-Feldern, die die Adressen darstellen, von denen dieser Computer erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7e59-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="e7e59-147">Netaddress ist ein Anbieter spezifisches **BSTR** , bestehend aus zwei Teil Zeichenfolgen, die durch einen Doppelpunkt (:) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="e7e59-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="e7e59-148">Die linke Teil Zeichenfolge gibt den Adresstyp an, und die Rechte Teil Zeichenfolge ist eine Zeichen folgen Darstellung einer Adresse dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="e7e59-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="e7e59-149">Beispielsweise weisen TCP/IP-Adressen folgendes Format auf: IP: 100.201.301.45.</span><span class="sxs-lookup"><span data-stu-id="e7e59-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="e7e59-150">Die IPX-typadressen weisen folgendes Format auf: IPX: 10.123456.80.</span><span class="sxs-lookup"><span data-stu-id="e7e59-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="e7e59-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-152">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="e7e59-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-153">**OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e7e59-153">**OperatingSystem**</span></span>
<span data-ttu-id="e7e59-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-155">Das auf diesem Computer verwendete Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="e7e59-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-157">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-158">**OperatingSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="e7e59-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="e7e59-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-160">Die Version des Betriebssystems, das auf diesem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7e59-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-162">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-163">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="e7e59-163">**Owner**</span></span>
<span data-ttu-id="e7e59-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-165">Die Person, der dieser Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e7e59-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="e7e59-166">Diese Person sollte auch über eine Lizenz zum Ausführen der installierten Software verfügen.</span><span class="sxs-lookup"><span data-stu-id="e7e59-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="e7e59-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-168">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="e7e59-169">**PrimaryUser**</span></span>
<span data-ttu-id="e7e59-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-171">Der Name der Kontaktperson (z. b. ein Administrator) für diesen Computer.</span><span class="sxs-lookup"><span data-stu-id="e7e59-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="e7e59-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-173">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-174">**Prozessor**</span><span class="sxs-lookup"><span data-stu-id="e7e59-174">**Processor**</span></span>
<span data-ttu-id="e7e59-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-176">Der Prozessortyp.</span><span class="sxs-lookup"><span data-stu-id="e7e59-176">The processor type.</span></span>

<dt>

<span data-ttu-id="e7e59-177">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-178">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="e7e59-179">**ProcessorCount**</span></span>
<span data-ttu-id="e7e59-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-181">Die Anzahl der installierten Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="e7e59-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="e7e59-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-183">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-184">**Rolle**</span><span class="sxs-lookup"><span data-stu-id="e7e59-184">**Role**</span></span>
<span data-ttu-id="e7e59-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-186">Die Rolle dieses Computers, z. b. Arbeitsstation, Server oder Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="e7e59-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="e7e59-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-188">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-189">**Website**</span><span class="sxs-lookup"><span data-stu-id="e7e59-189">**Site**</span></span>
<span data-ttu-id="e7e59-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-191">Der Globally Unique Identifier, der den Standort identifiziert, in dem dieser Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7e59-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="e7e59-192">Bei einem Standort handelt es sich um eine physische Region der guten Konnektivität in einem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e7e59-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="e7e59-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7e59-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-194">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7e59-195">**Storagecapacity**</span><span class="sxs-lookup"><span data-stu-id="e7e59-195">**StorageCapacity**</span></span>
<span data-ttu-id="e7e59-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e7e59-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="e7e59-197">Die Größe des Datenträgers in Megabyte.</span><span class="sxs-lookup"><span data-stu-id="e7e59-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="e7e59-198">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e7e59-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7e59-199">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7e59-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="e7e59-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7e59-200">Remarks</span></span>

<span data-ttu-id="e7e59-201">Verschiedene Anbieter können unterschiedliche Eigenschaften eines Computer Objekts verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e7e59-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="e7e59-202">Weitere Informationen finden Sie unter [ADSI-System Anbieter](adsi-system-providers.md).</span><span class="sxs-lookup"><span data-stu-id="e7e59-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="e7e59-203">Sie können ermitteln, welche Eigenschaften unterstützt werden, indem Sie die obligatorischen und optionalen Eigenschaften über die zugehörige Schema Klasse überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e7e59-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="e7e59-204">Weitere Informationen finden Sie unter [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e7e59-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="e7e59-205">Wenn Sie den Status eines Computers überprüfen oder den Vorgang zum Herunterfahren über das Netzwerk ausführen möchten, müssen Sie die [**iadscomputeroperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7e59-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="e7e59-206">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7e59-206">Examples</span></span>

<span data-ttu-id="e7e59-207">Im folgenden Visual Basic Codebeispiel werden Computer Eigenschaften überprüft, die vom ADSI WinNT-Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e7e59-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="e7e59-208">Im folgenden C++-Codebeispiel werden Computer Eigenschaften überprüft, die vom ADSI WinNT-Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e7e59-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="e7e59-209">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7e59-209">Requirements</span></span>



| <span data-ttu-id="e7e59-210">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7e59-210">Requirement</span></span> | <span data-ttu-id="e7e59-211">Wert</span><span class="sxs-lookup"><span data-stu-id="e7e59-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e59-212">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7e59-212">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e59-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7e59-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7e59-214">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7e59-214">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e59-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e59-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7e59-216">Header</span><span class="sxs-lookup"><span data-stu-id="e7e59-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7e59-217"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e59-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="e7e59-218">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e59-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e59-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e59-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7e59-220">IID</span><span class="sxs-lookup"><span data-stu-id="e7e59-220">IID</span></span><br/>                      | <span data-ttu-id="e7e59-221">IID \_ iadscomputer ist als EFE3CC70-1D9F-11CF-B1F3-02608C9E7553 definiert.</span><span class="sxs-lookup"><span data-stu-id="e7e59-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="e7e59-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7e59-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e59-223">**Iadscomputer**</span><span class="sxs-lookup"><span data-stu-id="e7e59-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="e7e59-224">ADSI-System Anbieter</span><span class="sxs-lookup"><span data-stu-id="e7e59-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="e7e59-225">**Iadsclass**</span><span class="sxs-lookup"><span data-stu-id="e7e59-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="e7e59-226">**Iadscomputeroperations**</span><span class="sxs-lookup"><span data-stu-id="e7e59-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="e7e59-227">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="e7e59-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





