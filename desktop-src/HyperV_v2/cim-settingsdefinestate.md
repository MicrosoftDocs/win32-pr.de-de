---
description: Ordnet Einstellungsdaten einem verwalteten Element zu.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: CIM_SettingsDefineState-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347481"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="8dab4-103">CIM \_ settingsdefinestate-Klasse</span><span class="sxs-lookup"><span data-stu-id="8dab4-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="8dab4-104">Ordnet Einstellungsdaten einem verwalteten Element zu.</span><span class="sxs-lookup"><span data-stu-id="8dab4-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dab4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dab4-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="8dab4-106">Member</span><span class="sxs-lookup"><span data-stu-id="8dab4-106">Members</span></span>

<span data-ttu-id="8dab4-107">Die **CIM \_ settingsdefinestate** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8dab4-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="8dab4-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dab4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dab4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dab4-109">Properties</span></span>

<span data-ttu-id="8dab4-110">Die **CIM \_ settingsdefinestate** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8dab4-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dab4-111">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="8dab4-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dab4-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="8dab4-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="8dab4-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dab4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dab4-114">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dab4-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dab4-115">Das verwaltete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8dab4-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="8dab4-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="8dab4-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dab4-117">Datentyp: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="8dab4-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="8dab4-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dab4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dab4-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dab4-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dab4-120">Die Einstellungsdaten in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8dab4-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dab4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dab4-121">Requirements</span></span>



| <span data-ttu-id="8dab4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dab4-122">Requirement</span></span> | <span data-ttu-id="8dab4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8dab4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dab4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dab4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8dab4-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8dab4-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8dab4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dab4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8dab4-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8dab4-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8dab4-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dab4-128">Namespace</span></span><br/>                | <span data-ttu-id="8dab4-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8dab4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8dab4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8dab4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dab4-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8dab4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dab4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8dab4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dab4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8dab4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

