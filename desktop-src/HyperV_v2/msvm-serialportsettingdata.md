---
description: Beschreibt die Einstellungsdaten für einen virtuellen seriellen Anschluss.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Msvm_SerialPortSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865512"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="02acf-103">MSVM \_ serialportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="02acf-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="02acf-104">Beschreibt die Einstellungsdaten für einen virtuellen seriellen Anschluss.</span><span class="sxs-lookup"><span data-stu-id="02acf-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="02acf-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="02acf-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02acf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="02acf-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="02acf-107">Member</span><span class="sxs-lookup"><span data-stu-id="02acf-107">Members</span></span>

<span data-ttu-id="02acf-108">Die **MSVM \_ serialportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02acf-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="02acf-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02acf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02acf-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02acf-110">Properties</span></span>

<span data-ttu-id="02acf-111">Die **MSVM \_ serialportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02acf-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02acf-112">**Debuggermode**</span><span class="sxs-lookup"><span data-stu-id="02acf-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02acf-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="02acf-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02acf-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02acf-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="02acf-115">**true** , wenn der Debuggermodus auf einem virtuellen seriellen Anschluss aktiviert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="02acf-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="02acf-116">Der Debugger-Modus verbessert die Verwendung eines Microsoft Windows-Kernel Debuggers über einen virtuellen seriellen Anschluss.</span><span class="sxs-lookup"><span data-stu-id="02acf-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02acf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02acf-117">Requirements</span></span>



| <span data-ttu-id="02acf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02acf-118">Requirement</span></span> | <span data-ttu-id="02acf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="02acf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02acf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02acf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02acf-121">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02acf-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="02acf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02acf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02acf-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="02acf-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="02acf-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="02acf-124">Namespace</span></span><br/>                | <span data-ttu-id="02acf-125">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="02acf-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02acf-126">MOF</span><span class="sxs-lookup"><span data-stu-id="02acf-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02acf-127"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="02acf-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02acf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="02acf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02acf-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02acf-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02acf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02acf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02acf-131">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="02acf-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




