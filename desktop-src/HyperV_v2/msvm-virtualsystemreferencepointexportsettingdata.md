---
description: Bietet zusätzliche Informationen, die mit der exportreferencepoint-Methode der MSVM \_ virtualsystemreferencepointservice-Klasse verwendet werden können.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Msvm_VirtualSystemReferencePointExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050700"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="a2cb7-103">MSVM \_ virtualsystemreferencepointexportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2cb7-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="a2cb7-104">Bietet zusätzliche Informationen, die mit der [**exportreferencepoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) -Methode der [**MSVM \_ virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md) -Klasse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="a2cb7-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2cb7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2cb7-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="a2cb7-107">Member</span><span class="sxs-lookup"><span data-stu-id="a2cb7-107">Members</span></span>

<span data-ttu-id="a2cb7-108">Die **MSVM \_ virtualsystemreferencepointexportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a2cb7-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a2cb7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2cb7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2cb7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2cb7-110">Properties</span></span>

<span data-ttu-id="a2cb7-111">Die **MSVM \_ virtualsystemreferencepointexportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2cb7-112">**Basereferencepoint**</span><span class="sxs-lookup"><span data-stu-id="a2cb7-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2cb7-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a2cb7-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="a2cb7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2cb7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2cb7-115">Der Pfad des Basis Verweis Punkts, in Bezug auf den Export, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="a2cb7-116">**Diskstoexport**</span><span class="sxs-lookup"><span data-stu-id="a2cb7-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2cb7-117">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a2cb7-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="a2cb7-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2cb7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2cb7-119">WMI-Instanz-IDs der Datenträger, für die Daten exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2cb7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2cb7-120">Requirements</span></span>



| <span data-ttu-id="a2cb7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2cb7-121">Requirement</span></span> | <span data-ttu-id="a2cb7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a2cb7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2cb7-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2cb7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2cb7-124">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2cb7-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a2cb7-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2cb7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2cb7-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a2cb7-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a2cb7-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2cb7-127">Namespace</span></span><br/>                | <span data-ttu-id="a2cb7-128">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2cb7-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2cb7-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a2cb7-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2cb7-130"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a2cb7-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2cb7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a2cb7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2cb7-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2cb7-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2cb7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2cb7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2cb7-134">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="a2cb7-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




