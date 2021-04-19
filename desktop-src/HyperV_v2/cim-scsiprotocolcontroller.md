---
description: Stellt einen Protokoll Controller dar, der eine SCSI-Schnittstelle verwaltet.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: CIM_SCSIProtocolController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356795"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="8ef67-103">CIM \_ scsiprotocolcontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="8ef67-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="8ef67-104">Stellt einen Protokoll Controller dar, der eine SCSI-Schnittstelle verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8ef67-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ef67-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="8ef67-106">Member</span><span class="sxs-lookup"><span data-stu-id="8ef67-106">Members</span></span>

<span data-ttu-id="8ef67-107">Die **CIM \_ scsiprotocolcontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8ef67-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="8ef67-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ef67-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ef67-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ef67-109">Properties</span></span>

<span data-ttu-id="8ef67-110">Die **CIM \_ scsiprotocolcontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8ef67-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ef67-111">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="8ef67-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef67-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef67-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef67-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8ef67-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ef67-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ scsiprotocolcontroller**".**Name**","**CIM \_ scsiprotocolcontroller**.**Othernameformat**")</span><span class="sxs-lookup"><span data-stu-id="8ef67-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8ef67-115">Das Format der **Name** -Eigenschaft von **CIM \_ scsiprotocolcontroller**.</span><span class="sxs-lookup"><span data-stu-id="8ef67-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8ef67-116">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="8ef67-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8ef67-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="8ef67-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="8ef67-118">**FC-WWN** (2)</span><span class="sxs-lookup"><span data-stu-id="8ef67-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="8ef67-119">**iSCSI-Name** (3)</span><span class="sxs-lookup"><span data-stu-id="8ef67-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8ef67-120">**Othernameformat**</span><span class="sxs-lookup"><span data-stu-id="8ef67-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef67-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8ef67-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef67-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8ef67-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ef67-123">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ scsiprotocolcontroller**".**Name**","**CIM \_ scsiprotocolcontroller**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="8ef67-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8ef67-124">Eine Beschreibung der **NameFormat** -Eigenschaft, wenn **NameFormat** auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8ef67-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ef67-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ef67-125">Requirements</span></span>



| <span data-ttu-id="8ef67-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ef67-126">Requirement</span></span> | <span data-ttu-id="8ef67-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8ef67-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef67-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ef67-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef67-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ef67-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8ef67-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ef67-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef67-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ef67-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8ef67-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ef67-132">Namespace</span></span><br/>                | <span data-ttu-id="8ef67-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8ef67-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8ef67-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8ef67-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ef67-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8ef67-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ef67-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8ef67-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ef67-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ef67-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ef67-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ef67-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef67-139">**CIM- \_ protocolcontroller**</span><span class="sxs-lookup"><span data-stu-id="8ef67-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

