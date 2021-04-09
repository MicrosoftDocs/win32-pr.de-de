---
description: Verbindet einen transparenten Überbrückungs Dienst mit einem dynamischen Forward-Eintrag (erlernte Mac-Adresse).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Msvm_TransparentBridgingDynamicForwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959186"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="e91b2-103">MSVM \_ transparentbridgingdynamicforwarding-Klasse</span><span class="sxs-lookup"><span data-stu-id="e91b2-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="e91b2-104">Verbindet einen transparenten Überbrückungs Dienst mit einem dynamischen Forward-Eintrag (erlernte Mac-Adresse).</span><span class="sxs-lookup"><span data-stu-id="e91b2-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="e91b2-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e91b2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91b2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e91b2-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e91b2-107">Member</span><span class="sxs-lookup"><span data-stu-id="e91b2-107">Members</span></span>

<span data-ttu-id="e91b2-108">Die **MSVM-Klasse " \_ transparentbridgingdynamicforwarding** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e91b2-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="e91b2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e91b2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e91b2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e91b2-110">Properties</span></span>

<span data-ttu-id="e91b2-111">Die **MSVM-Klasse " \_ transparentbridgingdynamicforwarding** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e91b2-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e91b2-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="e91b2-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91b2-113">Datentyp: **[ **MSVM \_ transparentbridgingservice**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="e91b2-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e91b2-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e91b2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91b2-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="e91b2-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e91b2-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ transparentbridgingservice**](msvm-transparentbridgingservice.md) ", die den transparenten Überbrückungs Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="e91b2-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="e91b2-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="e91b2-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91b2-118">Datentyp: **[ **MSVM \_ dynamicforwardingentry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="e91b2-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e91b2-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e91b2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91b2-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="e91b2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e91b2-121">Ein Verweis auf eine Instanz der [**MSVM \_ dynamicforwardingentry**](msvm-dynamicforwardingentry.md) -Klasse, die den dynamischen Weiterleitungs Eintrag der Weiterleitungs Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="e91b2-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e91b2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e91b2-122">Remarks</span></span>

<span data-ttu-id="e91b2-123">Der Zugriff auf die **MSVM-Klasse " \_ transparentbridgingdynamicforwarding** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="e91b2-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e91b2-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e91b2-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e91b2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e91b2-125">Requirements</span></span>



| <span data-ttu-id="e91b2-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e91b2-126">Requirement</span></span> | <span data-ttu-id="e91b2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e91b2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b2-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e91b2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e91b2-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e91b2-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e91b2-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e91b2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e91b2-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e91b2-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e91b2-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e91b2-132">Namespace</span></span><br/>                | <span data-ttu-id="e91b2-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e91b2-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e91b2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e91b2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e91b2-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e91b2-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e91b2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e91b2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e91b2-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e91b2-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e91b2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e91b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91b2-139">**CIM \_ transparentbridgingdynamicforwarding**</span><span class="sxs-lookup"><span data-stu-id="e91b2-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="e91b2-140">**CIM \_ transparentbridgingdynamicforwarding**</span><span class="sxs-lookup"><span data-stu-id="e91b2-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

