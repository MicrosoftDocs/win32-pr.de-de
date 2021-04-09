---
description: Die \_ WMI-Klasse der Win32 protocolbinding Association bezieht sich auf den Treiber, das Netzwerkprotokoll und den Netzwerkadapter auf Systemebene.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Win32_ProtocolBinding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860692"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="810c9-103">Win32 \_ protocolbinding-Klasse</span><span class="sxs-lookup"><span data-stu-id="810c9-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="810c9-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32 \_ protocolbinding** Association bezieht sich auf den Treiber, das Netzwerkprotokoll und den Netzwerkadapter auf Systemebene.</span><span class="sxs-lookup"><span data-stu-id="810c9-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="810c9-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="810c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="810c9-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="810c9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="810c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="810c9-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="810c9-108">Member</span><span class="sxs-lookup"><span data-stu-id="810c9-108">Members</span></span>

<span data-ttu-id="810c9-109">Die **Win32- \_ protocolbinding** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="810c9-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="810c9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="810c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="810c9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="810c9-111">Properties</span></span>

<span data-ttu-id="810c9-112">Die **Win32 \_ protocolbinding** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="810c9-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="810c9-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="810c9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c9-114">Datentyp: **Win32- \_ networkprotocol**</span><span class="sxs-lookup"><span data-stu-id="810c9-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="810c9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="810c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c9-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ networkprotocol")</span><span class="sxs-lookup"><span data-stu-id="810c9-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="810c9-117">Verweis auf die-Instanz, die das Protokoll darstellt, das mit dem System Treiber und dem Netzwerkadapter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="810c9-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="810c9-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="810c9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c9-119">Datentyp: **Win32 \_ System Driver**</span><span class="sxs-lookup"><span data-stu-id="810c9-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="810c9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="810c9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c9-121">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ System Driver")</span><span class="sxs-lookup"><span data-stu-id="810c9-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="810c9-122">Verweis auf die-Instanz, die den System Treiber darstellt, der den Netzwerkadapter über das Netzwerkprotokoll dieser Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="810c9-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="810c9-123">**Device**</span><span class="sxs-lookup"><span data-stu-id="810c9-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c9-124">Datentyp: **Win32- \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="810c9-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="810c9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="810c9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c9-126">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Network Adapter")</span><span class="sxs-lookup"><span data-stu-id="810c9-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="810c9-127">Eigenschaften des Netzwerkadapters, die auf dem Computersystem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="810c9-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="810c9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="810c9-128">Requirements</span></span>



| <span data-ttu-id="810c9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="810c9-129">Requirement</span></span> | <span data-ttu-id="810c9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="810c9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="810c9-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="810c9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="810c9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="810c9-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="810c9-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="810c9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="810c9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="810c9-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="810c9-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="810c9-135">Namespace</span></span><br/>                | <span data-ttu-id="810c9-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="810c9-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="810c9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="810c9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="810c9-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="810c9-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="810c9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="810c9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="810c9-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="810c9-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810c9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="810c9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810c9-142">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="810c9-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
