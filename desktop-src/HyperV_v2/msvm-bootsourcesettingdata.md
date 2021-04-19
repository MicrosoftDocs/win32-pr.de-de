---
description: Stellt die Parameter zum Festlegen der Start Quelle eines virtuellen Computers dar.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348822"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="adbdf-103">MSVM \_ bootsourcesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="adbdf-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="adbdf-104">Stellt die Parameter zum Festlegen der Start Quelle eines virtuellen Computers dar.</span><span class="sxs-lookup"><span data-stu-id="adbdf-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="adbdf-105">Diese Klasse wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="adbdf-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="adbdf-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="adbdf-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbdf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="adbdf-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="adbdf-108">Member</span><span class="sxs-lookup"><span data-stu-id="adbdf-108">Members</span></span>

<span data-ttu-id="adbdf-109">Die **MSVM \_ bootsourcesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="adbdf-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="adbdf-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adbdf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adbdf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adbdf-111">Properties</span></span>

<span data-ttu-id="adbdf-112">Die **MSVM \_ bootsourcesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="adbdf-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adbdf-113">**Bootsourcedescription**</span><span class="sxs-lookup"><span data-stu-id="adbdf-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-116">Die Beschreibung der von der Firmware bereitgestellten Start Quelle.</span><span class="sxs-lookup"><span data-stu-id="adbdf-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="adbdf-117">**Bootsourcetype**</span><span class="sxs-lookup"><span data-stu-id="adbdf-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="adbdf-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-120">Ein-Enumerationswert, der den Typ der Start Quelle angibt.</span><span class="sxs-lookup"><span data-stu-id="adbdf-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="adbdf-121">Dies sind gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="adbdf-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="adbdf-122">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="adbdf-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="adbdf-123">**Laufwerk** (1)</span><span class="sxs-lookup"><span data-stu-id="adbdf-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="adbdf-124">**Netzwerk** (2)</span><span class="sxs-lookup"><span data-stu-id="adbdf-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="adbdf-125">**Datei** (3)</span><span class="sxs-lookup"><span data-stu-id="adbdf-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="adbdf-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="adbdf-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-129">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="adbdf-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-130">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="adbdf-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="adbdf-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="adbdf-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-134">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="adbdf-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="adbdf-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="adbdf-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-138">Der Anzeige Name für diese Instanz von SettingData.</span><span class="sxs-lookup"><span data-stu-id="adbdf-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="adbdf-139">Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="adbdf-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="adbdf-140">(Hinweis: der Name muss innerhalb eines Namespace nicht eindeutig sein.)</span><span class="sxs-lookup"><span data-stu-id="adbdf-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="adbdf-141">**Firmwaredevicepath**</span><span class="sxs-lookup"><span data-stu-id="adbdf-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-144">Der Native Pfad, den die Firmware verwendet, um das Gerät zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="adbdf-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="adbdf-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="adbdf-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-148">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="adbdf-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-149">Im Gültigkeitsbereich des instanziierten Namespaces identifiziert InstanceId verdeckt und identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="adbdf-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="adbdf-150">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden: *OrgId*:*localId* , bei der *OrgId* und *localId* durch einen Doppelpunkt (:)) getrennt sind und *OrgId* einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäfts Entität ist, die die InstanceId erstellt oder definiert, oder bei der es sich um eine registrierte, von einer anerkannten globalen Autorität zugewiesene ID handelt.</span><span class="sxs-lookup"><span data-stu-id="adbdf-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="adbdf-151">(Diese Anforderung ähnelt dem Schema *Name* \_ *ClassName* -Struktur von Schema Klassennamen.) Außerdem darf *OrgId* keinen Doppelpunkt (:) enthalten, um die Eindeutigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="adbdf-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="adbdf-152">Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen *OrgId* und *localId* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="adbdf-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="adbdf-153">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="adbdf-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="adbdf-154">Wenn der oben genannte bevorzugte Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht für instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="adbdf-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="adbdf-155">Für von DMTF definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="adbdf-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="adbdf-156">**OptionalData**</span><span class="sxs-lookup"><span data-stu-id="adbdf-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-157">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="adbdf-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-159">**Qualifizierer: octetstring**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="adbdf-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-160">Optionale Daten, die von der Firmware bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="adbdf-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="adbdf-161">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="adbdf-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="adbdf-162">**Otherlocation**</span><span class="sxs-lookup"><span data-stu-id="adbdf-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adbdf-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="adbdf-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adbdf-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="adbdf-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adbdf-165">Die anderen Standortinformationen, sofern vorhanden, die die Firmware zur weiteren eindeutigen Identifizierung der Start Quelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="adbdf-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adbdf-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adbdf-166">Requirements</span></span>



| <span data-ttu-id="adbdf-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adbdf-167">Requirement</span></span> | <span data-ttu-id="adbdf-168">Wert</span><span class="sxs-lookup"><span data-stu-id="adbdf-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adbdf-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adbdf-169">Minimum supported client</span></span><br/> | <span data-ttu-id="adbdf-170">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="adbdf-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="adbdf-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adbdf-171">Minimum supported server</span></span><br/> | <span data-ttu-id="adbdf-172">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adbdf-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="adbdf-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="adbdf-173">Namespace</span></span><br/>                | <span data-ttu-id="adbdf-174">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="adbdf-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="adbdf-175">MOF</span><span class="sxs-lookup"><span data-stu-id="adbdf-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adbdf-176"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="adbdf-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="adbdf-177">DLL</span><span class="sxs-lookup"><span data-stu-id="adbdf-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbdf-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="adbdf-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="adbdf-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adbdf-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adbdf-180">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="adbdf-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="adbdf-181">[**CIM- \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="adbdf-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

