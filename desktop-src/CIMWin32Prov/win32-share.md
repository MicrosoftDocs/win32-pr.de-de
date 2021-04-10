---
description: Die Win32- \_ Freigabe Klasse stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows ausgeführt wird. Hierbei kann es sich um ein Laufwerk, einen Drucker, eine prozessübergreifende Kommunikation oder ein anderes shardgerät handeln. Weitere Informationen zum Abrufen von WMI-Klassen finden Sie unter Abrufen einer Klasse.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127320"
---
# <a name="win32_share-class"></a><span data-ttu-id="392d6-105">Win32- \_ Freigabe Klasse</span><span class="sxs-lookup"><span data-stu-id="392d6-105">Win32\_Share class</span></span>

<span data-ttu-id="392d6-106">Die **Win32- \_ Freigabe** Klasse stellt eine freigegebene Ressource auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="392d6-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="392d6-107">Hierbei kann es sich um ein Laufwerk, einen Drucker, eine prozessübergreifende Kommunikation oder ein anderes shardgerät handeln.</span><span class="sxs-lookup"><span data-stu-id="392d6-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="392d6-108">Weitere Informationen zum Abrufen von WMI-Klassen finden Sie unter [Abrufen einer Klasse](../wmisdk/retrieving-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="392d6-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="392d6-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="392d6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="392d6-110">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="392d6-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="392d6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="392d6-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="392d6-112">Member</span><span class="sxs-lookup"><span data-stu-id="392d6-112">Members</span></span>

<span data-ttu-id="392d6-113">Die **Win32- \_ Freigabe** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="392d6-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="392d6-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="392d6-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="392d6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="392d6-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="392d6-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="392d6-116">Methods</span></span>

<span data-ttu-id="392d6-117">Die **Win32- \_ Freigabe** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="392d6-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="392d6-118">Methode</span><span class="sxs-lookup"><span data-stu-id="392d6-118">Method</span></span>                                                             | <span data-ttu-id="392d6-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="392d6-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="392d6-120">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="392d6-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="392d6-121">Klassenmethode, die die Freigabe für eine Server Ressource initiiert.</span><span class="sxs-lookup"><span data-stu-id="392d6-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="392d6-122">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="392d6-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="392d6-123">Class-Methode, die einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers löscht, wobei Verbindungen mit der freigegebenen Ressource getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="392d6-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="392d6-124">**Getaccessmask**</span><span class="sxs-lookup"><span data-stu-id="392d6-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="392d6-125">Gibt die Zugriffsrechte für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in dessen Namen die Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="392d6-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="392d6-126">Sie sollten diese Methode anstelle der **AccessMask** -Eigenschaft verwenden, die immer **null** ist.</span><span class="sxs-lookup"><span data-stu-id="392d6-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="392d6-127">**Setshareingefo**</span><span class="sxs-lookup"><span data-stu-id="392d6-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="392d6-128">Klassenmethode, mit der die Parameter einer freigegebenen Ressource festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="392d6-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="392d6-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="392d6-129">Properties</span></span>

<span data-ttu-id="392d6-130">Die **Win32- \_ Freigabe** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="392d6-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="392d6-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="392d6-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="392d6-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-134">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="392d6-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="392d6-135">Diese Eigenschaft ist veraltet und wird nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="392d6-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="392d6-136">Verwenden Sie stattdessen die Win32-Methode " [**\_ share. getaccessmask**](getaccessmask-method-in-class-win32-share.md) ".</span><span class="sxs-lookup"><span data-stu-id="392d6-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="392d6-137">Der Wert der **AccessMask** -Eigenschaft wird von WMI auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="392d6-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="392d6-138">Weitere Informationen zum Festlegen des Zugriffs beim Erstellen einer Freigabe finden Sie unter der [**Create**](create-method-in-class-win32-share.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="392d6-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="392d6-139">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="392d6-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="392d6-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-142">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="392d6-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-143">Die Anzahl von gleichzeitigen Benutzern für diese Ressource ist beschränkt.</span><span class="sxs-lookup"><span data-stu-id="392d6-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="392d6-144">**True** gibt an, dass der Wert in der **MaximumAllowed** -Eigenschaft ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="392d6-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="392d6-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="392d6-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="392d6-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-148">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="392d6-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-149">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="392d6-149">A short textual description of the object.</span></span>

<span data-ttu-id="392d6-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="392d6-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="392d6-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="392d6-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="392d6-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-154">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="392d6-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-155">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="392d6-155">A textual description of the object.</span></span>

<span data-ttu-id="392d6-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="392d6-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="392d6-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="392d6-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-158">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="392d6-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-160">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="392d6-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-161">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="392d6-161">Indicates when the object was installed.</span></span> <span data-ttu-id="392d6-162">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="392d6-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="392d6-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="392d6-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="392d6-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="392d6-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="392d6-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-167">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="392d6-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-168">Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="392d6-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="392d6-169">Der Wert ist nur gültig, wenn die **AllowMaximum** -Eigenschaft auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="392d6-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="392d6-170">**Name**</span><span class="sxs-lookup"><span data-stu-id="392d6-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="392d6-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-173">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="392d6-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-174">Alias, der an einen Pfad übergeben wird, der als Freigabe auf einem Computersystem mit Windows eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="392d6-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="392d6-175">Windows 2008-Beispiel: " \\ Server01 \\ Public"-Windows Server 2008 erfordert, dass Sie die UNC-Datei im Namen platzieren.</span><span class="sxs-lookup"><span data-stu-id="392d6-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="392d6-176">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="392d6-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="392d6-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-179">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="392d6-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-180">Lokaler Pfad der Windows-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="392d6-180">Local path of the Windows share.</span></span>

<span data-ttu-id="392d6-181">Beispiel: "C: \\ Programmdateien"</span><span class="sxs-lookup"><span data-stu-id="392d6-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="392d6-182">**Status**</span><span class="sxs-lookup"><span data-stu-id="392d6-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="392d6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-185">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="392d6-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-186">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="392d6-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="392d6-187">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="392d6-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="392d6-188">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="392d6-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="392d6-189">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="392d6-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="392d6-190">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="392d6-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="392d6-191">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="392d6-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="392d6-192">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="392d6-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="392d6-193">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="392d6-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="392d6-194">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="392d6-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="392d6-195">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="392d6-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="392d6-196">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="392d6-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="392d6-197">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="392d6-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="392d6-198">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="392d6-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="392d6-199">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="392d6-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="392d6-200">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="392d6-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="392d6-201">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="392d6-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="392d6-202">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="392d6-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="392d6-203">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="392d6-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="392d6-204">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="392d6-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="392d6-205">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="392d6-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="392d6-206">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="392d6-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="392d6-207">**Type**</span><span class="sxs-lookup"><span data-stu-id="392d6-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="392d6-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="392d6-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="392d6-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="392d6-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="392d6-210">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Type")</span><span class="sxs-lookup"><span data-stu-id="392d6-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="392d6-211">Der Typ der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="392d6-211">Type of resource being shared.</span></span> <span data-ttu-id="392d6-212">Zu den Typen zählen: Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte.</span><span class="sxs-lookup"><span data-stu-id="392d6-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="392d6-213">**Laufwerk (0** )</span><span class="sxs-lookup"><span data-stu-id="392d6-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="392d6-214">**Druck Warteschlange** (1)</span><span class="sxs-lookup"><span data-stu-id="392d6-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="392d6-215">**Gerät** (2)</span><span class="sxs-lookup"><span data-stu-id="392d6-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="392d6-216">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="392d6-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="392d6-217">**Laufwerks Administrator** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="392d6-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="392d6-218">**Administrator der Druck Warteschlange** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="392d6-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="392d6-219">**Geräte Administrator** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="392d6-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="392d6-220">**IPC admin** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="392d6-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="392d6-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="392d6-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="392d6-222">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="392d6-222">Remarks</span></span>

<span data-ttu-id="392d6-223">Die **Win32- \_ Freigabe** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="392d6-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="392d6-224">Die Create-Methode in dieser Klasse ist eine statische Methode.</span><span class="sxs-lookup"><span data-stu-id="392d6-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="392d6-225">Die Methoden **Delete**, **getaccessmask** und **setshareinfo** sind alle Instanzmethoden.</span><span class="sxs-lookup"><span data-stu-id="392d6-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="392d6-226">Abhängig von den Sicherheits Berechtigungen können Sie möglicherweise nicht alle Eigenschaften dieser Klasse abrufen.</span><span class="sxs-lookup"><span data-stu-id="392d6-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="392d6-227">Beispielsweise können die Eigenschaften " **AllowMaximum**", " **MaximumAllowed**", " **path**" und " **Type** " NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="392d6-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="392d6-228">Im Allgemeinen können Poweruser und Administratoren alle Eigenschaftswerte abrufen.</span><span class="sxs-lookup"><span data-stu-id="392d6-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="392d6-229">Beispiele</span><span class="sxs-lookup"><span data-stu-id="392d6-229">Examples</span></span>

<span data-ttu-id="392d6-230">Im folgenden Skript Center-[Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) werden alle Freigaben auf einem Computer aufgelistet und alle Freigabe Berechtigungen für die einzelnen Freigaben aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="392d6-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="392d6-231">Die [Informationen zur Freigabe von Freigabe Informationen ähnlich wie Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample Queries Win32 \_ share und liefert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="392d6-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="392d6-232">Im folgenden PowerShell-Beispiel werden die Freigaben auf dem lokalen System angezeigt.</span><span class="sxs-lookup"><span data-stu-id="392d6-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="392d6-233">Wenn Sie den Filter genauer filtern möchten, können Sie alternativ den folgenden PowerShell-Code Ausschnitt verwenden:</span><span class="sxs-lookup"><span data-stu-id="392d6-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="392d6-234">Im folgenden VBScript-Beispiel werden die Freigaben auf dem lokalen System angezeigt.</span><span class="sxs-lookup"><span data-stu-id="392d6-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="392d6-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="392d6-235">Requirements</span></span>



| <span data-ttu-id="392d6-236">Anforderung</span><span class="sxs-lookup"><span data-stu-id="392d6-236">Requirement</span></span> | <span data-ttu-id="392d6-237">Wert</span><span class="sxs-lookup"><span data-stu-id="392d6-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="392d6-238">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="392d6-238">Minimum supported client</span></span><br/> | <span data-ttu-id="392d6-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="392d6-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="392d6-240">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="392d6-240">Minimum supported server</span></span><br/> | <span data-ttu-id="392d6-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="392d6-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="392d6-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="392d6-242">Namespace</span></span><br/>                | <span data-ttu-id="392d6-243">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="392d6-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="392d6-244">MOF</span><span class="sxs-lookup"><span data-stu-id="392d6-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="392d6-245"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="392d6-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="392d6-246">DLL</span><span class="sxs-lookup"><span data-stu-id="392d6-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="392d6-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="392d6-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="392d6-248">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="392d6-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392d6-249">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="392d6-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="392d6-250">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="392d6-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="392d6-251">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="392d6-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
