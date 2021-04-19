---
title: Win32_TSVmMetadataAssociation-Klasse
description: Stellt eine Zuordnung zwischen einer Remotedesktop virtuellen Maschine und ihren Metadateneigenschaften dar.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation-Klasse Remotedesktopdienste
- Win32_TSVmMetadataAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341586"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="87942-105">Win32- \_ TSVmMetadataAssociation-Klasse</span><span class="sxs-lookup"><span data-stu-id="87942-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="87942-106">Stellt eine Zuordnung zwischen einer Remotedesktop virtuellen Maschine und ihren Metadateneigenschaften dar.</span><span class="sxs-lookup"><span data-stu-id="87942-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="87942-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="87942-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87942-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="87942-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="87942-109">Member</span><span class="sxs-lookup"><span data-stu-id="87942-109">Members</span></span>

<span data-ttu-id="87942-110">Die **Win32- \_ TSVmMetadataAssociation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="87942-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="87942-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87942-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87942-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87942-112">Properties</span></span>

<span data-ttu-id="87942-113">Die **Win32- \_ TSVmMetadataAssociation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="87942-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87942-114">**MetadataItem**</span><span class="sxs-lookup"><span data-stu-id="87942-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87942-115">Datentyp: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="87942-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="87942-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="87942-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87942-117">Eine Instanz der [**Win32- \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) -Klasse, die die Metadaten für den virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="87942-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="87942-118">**Out-VM**</span><span class="sxs-lookup"><span data-stu-id="87942-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87942-119">Datentyp: **[ **Win32- \_ VM**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="87942-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="87942-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="87942-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87942-121">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87942-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="87942-122">Eine Instanz der Win32-Klasse " [**\_ ZVM**](win32-tsvm.md) ", die den virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="87942-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87942-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87942-123">Requirements</span></span>



| <span data-ttu-id="87942-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87942-124">Requirement</span></span> | <span data-ttu-id="87942-125">Wert</span><span class="sxs-lookup"><span data-stu-id="87942-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="87942-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87942-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87942-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="87942-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="87942-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87942-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87942-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87942-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="87942-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="87942-130">Namespace</span></span><br/>                | <span data-ttu-id="87942-131">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="87942-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="87942-132">MOF</span><span class="sxs-lookup"><span data-stu-id="87942-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87942-133"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="87942-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="87942-134">DLL</span><span class="sxs-lookup"><span data-stu-id="87942-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87942-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87942-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

