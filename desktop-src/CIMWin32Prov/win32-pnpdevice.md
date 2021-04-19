---
description: Die \_ WMI-Klasse für die Win32-pnpdevice-Zuordnung verknüpft ein Gerät (bekannt als pntztity) und die Funktion Configuration Manager, die es ausführt.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346458"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="3cafe-103">Win32- \_ pnpdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cafe-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="3cafe-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32- \_ pnpdevice** -Zuordnung verknüpft ein Gerät (bekannt als pntztity) und die Funktion Configuration Manager, die es ausführt.</span><span class="sxs-lookup"><span data-stu-id="3cafe-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="3cafe-105">Die Funktion wird durch eine Unterklasse des logischen Geräts dargestellt, das deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3cafe-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="3cafe-106">Beispielsweise eine [**Win32- \_ Tastatur**](win32-keyboard.md) oder eine [**Win32 \_ diskdrive**](win32-diskdrive.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="3cafe-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="3cafe-107">Beide referenzierten Objekte stellen dasselbe zugrunde liegende System Gerät dar. Änderungen an der Ressourcen Zuordnung auf der pnptity-Seite wirken sich auf das zugehörige Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="3cafe-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="3cafe-108">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cafe-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3cafe-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3cafe-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cafe-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cafe-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="3cafe-111">Member</span><span class="sxs-lookup"><span data-stu-id="3cafe-111">Members</span></span>

<span data-ttu-id="3cafe-112">Die **Win32- \_ pnpdevice** -Klasse verfügt über diese Typen von mempdevice:</span><span class="sxs-lookup"><span data-stu-id="3cafe-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3cafe-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cafe-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cafe-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cafe-114">Properties</span></span>

<span data-ttu-id="3cafe-115">Die **Win32- \_ pnpdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cafe-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cafe-116">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="3cafe-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cafe-117">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3cafe-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3cafe-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cafe-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cafe-119">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="3cafe-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="3cafe-120">Verweis auf die [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanz, die die Eigenschaften des logischen Geräts darstellt, die dem Plug & Play-Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3cafe-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="3cafe-121">**Systemelement**</span><span class="sxs-lookup"><span data-stu-id="3cafe-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cafe-122">Datentyp: **Win32 \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="3cafe-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="3cafe-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cafe-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cafe-124">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ pnptity")</span><span class="sxs-lookup"><span data-stu-id="3cafe-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="3cafe-125">Verweis auf die [**Win32- \_ pnptity**](win32-pnpentity.md) -Instanz, die das Plug & Play Gerät darstellt, das dem logischen Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3cafe-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cafe-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cafe-126">Requirements</span></span>



| <span data-ttu-id="3cafe-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cafe-127">Requirement</span></span> | <span data-ttu-id="3cafe-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3cafe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cafe-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cafe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3cafe-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cafe-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cafe-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cafe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3cafe-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cafe-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cafe-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cafe-133">Namespace</span></span><br/>                | <span data-ttu-id="3cafe-134">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3cafe-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3cafe-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3cafe-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cafe-136"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3cafe-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cafe-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3cafe-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cafe-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cafe-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cafe-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cafe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cafe-140">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="3cafe-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
