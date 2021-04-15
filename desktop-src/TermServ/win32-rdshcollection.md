---
title: Win32_RDSHCollection-Klasse
description: Verwaltet eine Auflistung von Remotedesktop Sitzungs Hosts.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection-Klasse Remotedesktopdienste
- Win32_RDSHCollection Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477079"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="20aab-105">Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="20aab-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="20aab-106">Verwaltet eine Auflistung von Remotedesktop Sitzungs Hosts.</span><span class="sxs-lookup"><span data-stu-id="20aab-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="20aab-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="20aab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20aab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="20aab-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="20aab-109">Member</span><span class="sxs-lookup"><span data-stu-id="20aab-109">Members</span></span>

<span data-ttu-id="20aab-110">Die **Win32 \_ rdshcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="20aab-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="20aab-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="20aab-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="20aab-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20aab-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20aab-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="20aab-113">Methods</span></span>

<span data-ttu-id="20aab-114">Die **Win32 \_ rdshcollection** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="20aab-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="20aab-115">Methode</span><span class="sxs-lookup"><span data-stu-id="20aab-115">Method</span></span>                                                                      | <span data-ttu-id="20aab-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20aab-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aab-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="20aab-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="20aab-118">Ruft einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshcollection** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="20aab-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="20aab-119">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="20aab-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="20aab-120">Ruft den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshcollection** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="20aab-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="20aab-121">**Keyvaluecompareandset**</span><span class="sxs-lookup"><span data-stu-id="20aab-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="20aab-122">Vergleicht den angegebenen Schlüssel in der Auflistung mit einem comparand. Stimmen Sie zu, wird der Schlüssel auf einen neuen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="20aab-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="20aab-123">Wenn der Schlüssel nicht vorhanden ist, fügt die Methode den Schlüssel in die Auflistung ein.</span><span class="sxs-lookup"><span data-stu-id="20aab-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="20aab-124">**Keyvaluedelete**</span><span class="sxs-lookup"><span data-stu-id="20aab-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="20aab-125">Löscht den angegebenen Schlüssel (und zugeordneten Wert) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="20aab-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="20aab-126">**Keyvalueget**</span><span class="sxs-lookup"><span data-stu-id="20aab-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="20aab-127">Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="20aab-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="20aab-128">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="20aab-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="20aab-129">Aktualisiert einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshcollection** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="20aab-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="20aab-130">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="20aab-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="20aab-131">Aktualisiert den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshcollection** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="20aab-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="20aab-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20aab-132">Properties</span></span>

<span data-ttu-id="20aab-133">Die **Win32 \_ rdshcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="20aab-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20aab-134">**Alias**</span><span class="sxs-lookup"><span data-stu-id="20aab-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aab-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="20aab-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aab-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="20aab-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="20aab-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="20aab-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="20aab-138">Ruft den Alias der Auflistung ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="20aab-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="20aab-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20aab-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aab-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="20aab-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aab-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="20aab-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="20aab-142">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20aab-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20aab-143">Ruft die Beschreibung der Auflistung ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="20aab-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="20aab-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="20aab-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aab-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="20aab-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aab-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="20aab-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20aab-147">Ruft den Namen der Auflistung ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="20aab-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="20aab-148">**Type**</span><span class="sxs-lookup"><span data-stu-id="20aab-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aab-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aab-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aab-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="20aab-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20aab-151">**Windows Server 2012 R2 und Windows Server 2012:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20aab-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="20aab-152">Der Typ der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="20aab-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="20aab-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regulär** (0)</span><span class="sxs-lookup"><span data-stu-id="20aab-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aab-154">(2)</span><span class="sxs-lookup"><span data-stu-id="20aab-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="20aab-155">Reserviert</span><span class="sxs-lookup"><span data-stu-id="20aab-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="20aab-156">(3)</span><span class="sxs-lookup"><span data-stu-id="20aab-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="20aab-157">Reserviert</span><span class="sxs-lookup"><span data-stu-id="20aab-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="20aab-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**Manualpersonal** (4)</span><span class="sxs-lookup"><span data-stu-id="20aab-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="20aab-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Autopersonal** (5)</span><span class="sxs-lookup"><span data-stu-id="20aab-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="20aab-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="20aab-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="20aab-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20aab-161">Requirements</span></span>



| <span data-ttu-id="20aab-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20aab-162">Requirement</span></span> | <span data-ttu-id="20aab-163">Wert</span><span class="sxs-lookup"><span data-stu-id="20aab-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="20aab-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20aab-164">Minimum supported client</span></span><br/> | <span data-ttu-id="20aab-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="20aab-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="20aab-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20aab-166">Minimum supported server</span></span><br/> | <span data-ttu-id="20aab-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20aab-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="20aab-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="20aab-168">Namespace</span></span><br/>                | <span data-ttu-id="20aab-169">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="20aab-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="20aab-170">MOF</span><span class="sxs-lookup"><span data-stu-id="20aab-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20aab-171"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="20aab-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="20aab-172">DLL</span><span class="sxs-lookup"><span data-stu-id="20aab-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20aab-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20aab-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="20aab-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20aab-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20aab-175">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="20aab-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

