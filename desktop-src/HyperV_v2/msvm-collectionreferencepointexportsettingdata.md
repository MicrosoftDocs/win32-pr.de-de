---
description: Exportieren von Einstellungsdaten, die an die exportreferencepoint-Methode der MSVM \_ collectionreferencepointservice-Klasse übermittelt werden sollen.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Msvm_CollectionReferencePointExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350078"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="99ee9-103">MSVM \_ collectionreferencepointexportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="99ee9-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="99ee9-104">Exportieren von Einstellungsdaten, die an die [**exportreferencepoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) -Methode der [**MSVM \_ collectionreferencepointservice**](msvm-collectionreferencepointservice.md) -Klasse übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99ee9-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="99ee9-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99ee9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ee9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="99ee9-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="99ee9-107">Member</span><span class="sxs-lookup"><span data-stu-id="99ee9-107">Members</span></span>

<span data-ttu-id="99ee9-108">Die **MSVM \_ collectionreferencepointexportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="99ee9-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="99ee9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ee9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99ee9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99ee9-110">Properties</span></span>

<span data-ttu-id="99ee9-111">Die **MSVM \_ collectionreferencepointexportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99ee9-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99ee9-112">**Basereferencepointcollection**</span><span class="sxs-lookup"><span data-stu-id="99ee9-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99ee9-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="99ee9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99ee9-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="99ee9-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="99ee9-115">Der Pfad zu einer [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) -Instanz, die die Basis-Verweis Punkt Auflistung darstellt, die für den differenziellen Export verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99ee9-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="99ee9-116">**Virtualmachinestodiskstoexport**</span><span class="sxs-lookup"><span data-stu-id="99ee9-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99ee9-117">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="99ee9-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="99ee9-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="99ee9-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="99ee9-119">Qualifizierer: **hypervembeddebug** ("MSVM \_ virtualmachinetodisks")</span><span class="sxs-lookup"><span data-stu-id="99ee9-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="99ee9-120">Eine Liste der "VirtualMachines to diskstoexport"-Karteninformationen, für die Daten exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="99ee9-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99ee9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99ee9-121">Requirements</span></span>



| <span data-ttu-id="99ee9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99ee9-122">Requirement</span></span> | <span data-ttu-id="99ee9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="99ee9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99ee9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99ee9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99ee9-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99ee9-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="99ee9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99ee9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99ee9-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="99ee9-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="99ee9-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="99ee9-128">Namespace</span></span><br/>                | <span data-ttu-id="99ee9-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="99ee9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="99ee9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="99ee9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99ee9-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="99ee9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99ee9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="99ee9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99ee9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99ee9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99ee9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99ee9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ee9-135">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="99ee9-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




