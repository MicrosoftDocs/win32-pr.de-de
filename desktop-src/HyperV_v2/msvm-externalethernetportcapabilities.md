---
description: Beschreibt die Funktionen des zugeordneten MSVM \_ externalethernetport.
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Msvm_ExternalEthernetPortCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862944"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="abf91-103">MSVM \_ externalethernetportfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="abf91-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="abf91-104">Beschreibt die Funktionen des zugeordneten [**MSVM \_ externalethernetport**](msvm-externalethernetport.md).</span><span class="sxs-lookup"><span data-stu-id="abf91-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="abf91-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abf91-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf91-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="abf91-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="abf91-107">Member</span><span class="sxs-lookup"><span data-stu-id="abf91-107">Members</span></span>

<span data-ttu-id="abf91-108">Die **MSVM \_ externalethernetportfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="abf91-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="abf91-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abf91-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abf91-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abf91-110">Properties</span></span>

<span data-ttu-id="abf91-111">Die **MSVM \_ externalethernetportfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abf91-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abf91-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="abf91-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf91-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="abf91-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf91-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abf91-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abf91-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="abf91-115">A short description of the object.</span></span> <span data-ttu-id="abf91-116">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abf91-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="abf91-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abf91-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf91-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="abf91-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf91-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abf91-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abf91-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="abf91-120">A description of the object.</span></span> <span data-ttu-id="abf91-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "beschreibt die Funktionen des Microsoft-externen Ethernet-Ports" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abf91-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="abf91-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="abf91-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf91-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="abf91-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf91-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abf91-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abf91-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="abf91-125">A display name for the object.</span></span> <span data-ttu-id="abf91-126">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abf91-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="abf91-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="abf91-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf91-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="abf91-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf91-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abf91-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abf91-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="abf91-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="abf91-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="abf91-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="abf91-132">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="abf91-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="abf91-133">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="abf91-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf91-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="abf91-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abf91-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abf91-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abf91-136">Ein boolescher Wert, der angibt, ob die e/a-Virtualisierung (IOV) vom Netzwerkadapter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="abf91-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="abf91-137">Wenn der Wert **true** ist, wird IOV vom Netzwerkadapter unterstützt, und die **iovsupporwerons** -Eigenschaft ist leer.</span><span class="sxs-lookup"><span data-stu-id="abf91-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="abf91-138">Andernfalls gibt die **iovsuppor-** Eigenschaft die Gründe dafür, warum IOV nicht unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="abf91-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="abf91-139">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="abf91-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf91-140">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="abf91-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="abf91-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abf91-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abf91-142">Ein Array von Zeichen folgen, das die möglichen Gründe angibt, warum IOV nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="abf91-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="abf91-143">Wenn der Wert von **iovsupport** den Wert **true** hat, ist dieses Array leer.</span><span class="sxs-lookup"><span data-stu-id="abf91-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abf91-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abf91-144">Requirements</span></span>



| <span data-ttu-id="abf91-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abf91-145">Requirement</span></span> | <span data-ttu-id="abf91-146">Wert</span><span class="sxs-lookup"><span data-stu-id="abf91-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf91-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abf91-147">Minimum supported client</span></span><br/> | <span data-ttu-id="abf91-148">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abf91-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="abf91-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abf91-149">Minimum supported server</span></span><br/> | <span data-ttu-id="abf91-150">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abf91-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abf91-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="abf91-151">Namespace</span></span><br/>                | <span data-ttu-id="abf91-152">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="abf91-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="abf91-153">MOF</span><span class="sxs-lookup"><span data-stu-id="abf91-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abf91-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="abf91-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abf91-155">DLL</span><span class="sxs-lookup"><span data-stu-id="abf91-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abf91-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abf91-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

