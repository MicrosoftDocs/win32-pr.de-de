---
description: Stellt die Parameter zum Kopieren einer Datei vom Host in den Gast dar.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355348"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="1d56b-103">MSVM \_ copyfiledeguestsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="1d56b-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="1d56b-104">Stellt die Parameter zum Kopieren einer Datei vom Host in den Gast dar.</span><span class="sxs-lookup"><span data-stu-id="1d56b-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="1d56b-105">Diese Klasse wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1d56b-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="1d56b-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1d56b-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d56b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d56b-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="1d56b-108">Member</span><span class="sxs-lookup"><span data-stu-id="1d56b-108">Members</span></span>

<span data-ttu-id="1d56b-109">Die **MSVM \_ copyfiletoguestsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1d56b-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1d56b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d56b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d56b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d56b-111">Properties</span></span>

<span data-ttu-id="1d56b-112">Die **MSVM \_ copyfiledeguestsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d56b-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d56b-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d56b-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d56b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-116">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1d56b-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d56b-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-118">**"Kreatefullpath"**</span><span class="sxs-lookup"><span data-stu-id="1d56b-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1d56b-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-121">Gibt an, ob fehlende Verzeichnisse im Pfad der Zieldatei vor dem Kopieren der Datei erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d56b-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d56b-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d56b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-125">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d56b-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="1d56b-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d56b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-129">Der komplette Pfad der Zieldatei, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d56b-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="1d56b-130">Diese Zieldatei muss für den Gast zugänglich sein und Umgebungsvariablen enthalten können, die vom Gast erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="1d56b-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="1d56b-131">Wenn es sich bei dem angegebenen Pfad um ein vorhandenes Verzeichnis im Gast Verzeichnis handelt, wird die Zieldatei in diesem Verzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d56b-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="1d56b-132">In diesem Fall wird der Dateiname aus **SourcePath** als Ziel Dateiname verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d56b-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1d56b-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d56b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-136">Der Anzeige Name für diese Instanz von SettingData.</span><span class="sxs-lookup"><span data-stu-id="1d56b-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="1d56b-137">Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d56b-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="1d56b-138">(Hinweis: der Name muss innerhalb eines Namespace nicht eindeutig sein.)</span><span class="sxs-lookup"><span data-stu-id="1d56b-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d56b-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d56b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-142">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1d56b-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-143">Im Gültigkeitsbereich des instanziierten Namespaces identifiziert InstanceId verdeckt und identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1d56b-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1d56b-144">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden: *OrgId*:*localId* , bei der *OrgId* und *localId* durch einen Doppelpunkt (:)) getrennt sind und *OrgId* einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäfts Entität ist, die die InstanceId erstellt oder definiert, oder bei der es sich um eine registrierte, von einer anerkannten globalen Autorität zugewiesene ID handelt.</span><span class="sxs-lookup"><span data-stu-id="1d56b-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="1d56b-145">(Diese Anforderung ähnelt dem Schema *Name* \_ *ClassName* -Struktur von Schema Klassennamen.) Außerdem darf *OrgId* keinen Doppelpunkt (:) enthalten, um die Eindeutigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d56b-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="1d56b-146">Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen *OrgId* und *localId* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d56b-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="1d56b-147">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1d56b-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="1d56b-148">Wenn der oben genannte bevorzugte Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht für instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d56b-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="1d56b-149">Für von DMTF definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1d56b-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-150">**Überschreiben vorhanden**</span><span class="sxs-lookup"><span data-stu-id="1d56b-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-151">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1d56b-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-153">Gibt an, ob eine vorhandene Zieldatei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="1d56b-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="1d56b-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="1d56b-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d56b-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1d56b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d56b-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1d56b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d56b-157">Der gesamte Pfad der Quelldatei, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d56b-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="1d56b-158">Auf diese Quelldatei muss der Hyper-v-Host zugreifen können, und Sie kann Umgebungsvariablen enthalten, die vom Hyper-v-Host erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="1d56b-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d56b-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d56b-159">Requirements</span></span>



| <span data-ttu-id="1d56b-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d56b-160">Requirement</span></span> | <span data-ttu-id="1d56b-161">Wert</span><span class="sxs-lookup"><span data-stu-id="1d56b-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d56b-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d56b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1d56b-163">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1d56b-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1d56b-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d56b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1d56b-165">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d56b-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d56b-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d56b-166">Namespace</span></span><br/>                | <span data-ttu-id="1d56b-167">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1d56b-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d56b-168">MOF</span><span class="sxs-lookup"><span data-stu-id="1d56b-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d56b-169"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1d56b-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d56b-170">DLL</span><span class="sxs-lookup"><span data-stu-id="1d56b-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d56b-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d56b-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d56b-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d56b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d56b-173">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="1d56b-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="1d56b-174">[**CIM- \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d56b-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

