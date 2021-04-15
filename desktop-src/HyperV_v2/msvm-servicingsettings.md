---
description: Enthält Einstellungen, die während des Wartungs Vorgangs verwendet werden.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Msvm_ServicingSettings-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485270"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="20b51-103">MSVM \_ servicingsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="20b51-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="20b51-104">Enthält Einstellungen, die während des Wartungs Vorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20b51-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="20b51-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="20b51-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b51-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="20b51-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="20b51-107">Member</span><span class="sxs-lookup"><span data-stu-id="20b51-107">Members</span></span>

<span data-ttu-id="20b51-108">Die **MSVM \_ servicingsettings** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="20b51-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="20b51-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20b51-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20b51-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20b51-110">Properties</span></span>

<span data-ttu-id="20b51-111">Die **MSVM \_ servicingsettings** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="20b51-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20b51-112">**Version**</span><span class="sxs-lookup"><span data-stu-id="20b51-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20b51-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="20b51-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20b51-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="20b51-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20b51-115">Enthält die Version der Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="20b51-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20b51-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20b51-116">Requirements</span></span>



| <span data-ttu-id="20b51-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20b51-117">Requirement</span></span> | <span data-ttu-id="20b51-118">Wert</span><span class="sxs-lookup"><span data-stu-id="20b51-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b51-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20b51-119">Minimum supported client</span></span><br/> | <span data-ttu-id="20b51-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20b51-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20b51-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20b51-121">Minimum supported server</span></span><br/> | <span data-ttu-id="20b51-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20b51-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20b51-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="20b51-123">Namespace</span></span><br/>                | <span data-ttu-id="20b51-124">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="20b51-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20b51-125">MOF</span><span class="sxs-lookup"><span data-stu-id="20b51-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20b51-126"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="20b51-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20b51-127">DLL</span><span class="sxs-lookup"><span data-stu-id="20b51-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b51-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20b51-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




