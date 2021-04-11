---
description: Die Win32 \_ clustershare-Klasse stellt eine freigegebene Ressource auf einem Cluster dar.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127353"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="04433-103">Win32 \_ clustershare-Klasse</span><span class="sxs-lookup"><span data-stu-id="04433-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="04433-104">\[Die **Win32 \_ clustershare** -Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="04433-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="04433-105">Verwenden Sie stattdessen die Klassen " [**MSFT \_ FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) " und " [**MSFT \_ smfileshare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) ".\]</span><span class="sxs-lookup"><span data-stu-id="04433-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="04433-106">Die Win32 \_ clustershare-Klasse stellt eine freigegebene Ressource auf einem Cluster dar.</span><span class="sxs-lookup"><span data-stu-id="04433-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="04433-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="04433-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04433-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04433-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
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
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="04433-109">Member</span><span class="sxs-lookup"><span data-stu-id="04433-109">Members</span></span>

<span data-ttu-id="04433-110">Die **Win32 \_ clustershare** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="04433-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="04433-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="04433-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="04433-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04433-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04433-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="04433-113">Methods</span></span>

<span data-ttu-id="04433-114">Die **Win32- \_ clustershare** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="04433-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="04433-115">Methode</span><span class="sxs-lookup"><span data-stu-id="04433-115">Method</span></span>                                                    | <span data-ttu-id="04433-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04433-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="04433-117">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="04433-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="04433-118">Erstellt eine neue **Win32- \_ clustershare** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="04433-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="04433-119">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="04433-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="04433-120">Löscht eine **Win32- \_ clustershare** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="04433-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="04433-121">**Getaccessmask**</span><span class="sxs-lookup"><span data-stu-id="04433-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="04433-122">Gibt eine Bitmap mit den Zugriffsrechten für die Freigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="04433-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="04433-123">**Setshareingefo**</span><span class="sxs-lookup"><span data-stu-id="04433-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="04433-124">Legt die Parameter der freigegebenen Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="04433-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="04433-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04433-125">Properties</span></span>

<span data-ttu-id="04433-126">Die **Win32 \_ clustershare** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="04433-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04433-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="04433-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04433-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04433-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-130">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="04433-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="04433-131">Diese Eigenschaft ist veraltet und wird nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="04433-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="04433-132">Verwenden Sie stattdessen die Win32-Methode " [**\_ share. getaccessmask**](getaccessmask-method-in-class-win32-share.md) ".</span><span class="sxs-lookup"><span data-stu-id="04433-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="04433-133">Der Wert der **AccessMask** -Eigenschaft wird von WMI auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04433-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="04433-134">Weitere Informationen zum Festlegen des Zugriffs beim Erstellen einer Freigabe finden Sie unter der [**Create**](create-method-in-class-win32-share.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="04433-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="04433-135">Diese Eigenschaft wird von der [**Win32- \_ Freigabe**](win32-share.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-136">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="04433-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="04433-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04433-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="04433-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="04433-140">Die Anzahl von gleichzeitigen Benutzern für diese Ressource ist beschränkt.</span><span class="sxs-lookup"><span data-stu-id="04433-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="04433-141">**True** gibt an, dass der Wert in der **MaximumAllowed** -Eigenschaft ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="04433-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="04433-142">Diese Eigenschaft wird von der [**Win32- \_ Freigabe**](win32-share.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="04433-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="04433-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04433-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-146">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="04433-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="04433-147">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="04433-147">A short textual description of the object.</span></span>

<span data-ttu-id="04433-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04433-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="04433-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04433-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-152">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="04433-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="04433-153">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="04433-153">A textual description of the object.</span></span>

<span data-ttu-id="04433-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="04433-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-156">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="04433-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04433-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-158">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="04433-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="04433-159">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="04433-159">Indicates when the object was installed.</span></span> <span data-ttu-id="04433-160">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="04433-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="04433-161">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="04433-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04433-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04433-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-165">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="04433-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="04433-166">Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="04433-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="04433-167">Der Wert ist nur gültig, wenn die **AllowMaximum** -Eigenschaft auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="04433-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="04433-168">Diese Eigenschaft wird von der [**Win32- \_ Freigabe**](win32-share.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-169">**Name**</span><span class="sxs-lookup"><span data-stu-id="04433-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="04433-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04433-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-172">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="04433-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="04433-173">Alias, der an einen Pfad übergeben wird, der als Freigabe auf einem Computersystem mit Windows eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="04433-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="04433-174">Windows 2008-Beispiel: " \\ Server01 \\ Public"-Windows Server 2008 erfordert, dass Sie die UNC-Datei im Namen platzieren.</span><span class="sxs-lookup"><span data-stu-id="04433-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="04433-175">Diese Eigenschaft wird von der [**Win32- \_ Freigabe**](win32-share.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-176">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="04433-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="04433-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04433-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-179">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="04433-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="04433-180">Lokaler Pfad der Windows-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="04433-180">Local path of the Windows share.</span></span>

<span data-ttu-id="04433-181">Beispiel: "C: \\ Programmdateien"</span><span class="sxs-lookup"><span data-stu-id="04433-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="04433-182">Diese Eigenschaft wird von der [**Win32- \_ Freigabe**](win32-share.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="04433-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="04433-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="04433-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04433-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-186">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Servername"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ Servername")</span><span class="sxs-lookup"><span data-stu-id="04433-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="04433-187">Der Cluster Server, auf dem die Freigabe gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="04433-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="04433-188">**Status**</span><span class="sxs-lookup"><span data-stu-id="04433-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="04433-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04433-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-191">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="04433-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="04433-192">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="04433-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="04433-193">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="04433-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="04433-194">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="04433-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="04433-195">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="04433-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="04433-196">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="04433-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="04433-197">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="04433-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="04433-198">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="04433-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="04433-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="04433-200">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="04433-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="04433-201">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="04433-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="04433-202">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="04433-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="04433-203">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="04433-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04433-204">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="04433-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="04433-205">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="04433-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="04433-206">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="04433-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="04433-207">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="04433-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="04433-208">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="04433-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="04433-209">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="04433-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="04433-210">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="04433-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="04433-211">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="04433-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="04433-212">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="04433-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04433-213">**Type**</span><span class="sxs-lookup"><span data-stu-id="04433-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04433-214">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04433-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04433-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04433-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04433-216">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**share \_ Info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Type")</span><span class="sxs-lookup"><span data-stu-id="04433-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="04433-217">Der Typ der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="04433-217">Type of resource being shared.</span></span> <span data-ttu-id="04433-218">Zu den Typen zählen: Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte.</span><span class="sxs-lookup"><span data-stu-id="04433-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="04433-219">Diese Eigenschaft wird von der [**Win32- \_ Freigabe**](win32-share.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="04433-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="04433-220">**Laufwerk (0** )</span><span class="sxs-lookup"><span data-stu-id="04433-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="04433-221">**Druck Warteschlange** (1)</span><span class="sxs-lookup"><span data-stu-id="04433-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="04433-222">**Gerät** (2)</span><span class="sxs-lookup"><span data-stu-id="04433-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="04433-223">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="04433-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="04433-224">**Laufwerks Administrator** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="04433-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="04433-225">**Administrator der Druck Warteschlange** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="04433-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="04433-226">**Geräte Administrator** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="04433-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="04433-227">**IPC admin** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="04433-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="04433-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="04433-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="04433-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04433-229">Requirements</span></span>



| <span data-ttu-id="04433-230">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04433-230">Requirement</span></span> | <span data-ttu-id="04433-231">Wert</span><span class="sxs-lookup"><span data-stu-id="04433-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04433-232">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04433-232">Minimum supported client</span></span><br/> | <span data-ttu-id="04433-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04433-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="04433-234">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04433-234">Minimum supported server</span></span><br/> | <span data-ttu-id="04433-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04433-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="04433-236">Namespace</span><span class="sxs-lookup"><span data-stu-id="04433-236">Namespace</span></span><br/>                | <span data-ttu-id="04433-237">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="04433-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04433-238">MOF</span><span class="sxs-lookup"><span data-stu-id="04433-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04433-239"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="04433-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04433-240">DLL</span><span class="sxs-lookup"><span data-stu-id="04433-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04433-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04433-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04433-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04433-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04433-243">**Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="04433-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

