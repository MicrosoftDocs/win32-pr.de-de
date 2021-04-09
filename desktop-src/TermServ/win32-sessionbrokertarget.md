---
title: Win32_SessionBrokerTarget-Klasse
description: Definiert die Abfrage für ein Sitzungs Broker Ziel.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTarget-Klasse Remotedesktopdienste
- Win32_SessionBrokerTarget Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859259"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="13bb6-105">Win32- \_ Klasse "sessionbrokertarget"</span><span class="sxs-lookup"><span data-stu-id="13bb6-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="13bb6-106">Definiert die Abfrage für ein Sitzungs Broker Ziel.</span><span class="sxs-lookup"><span data-stu-id="13bb6-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="13bb6-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13bb6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bb6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13bb6-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="13bb6-109">Member</span><span class="sxs-lookup"><span data-stu-id="13bb6-109">Members</span></span>

<span data-ttu-id="13bb6-110">Die Win32-Klasse " **\_ sessionbrokertarget** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13bb6-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="13bb6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13bb6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13bb6-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13bb6-112">Properties</span></span>

<span data-ttu-id="13bb6-113">Die Win32-Klasse " **\_ sessionbrokertarget** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13bb6-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13bb6-114">**Umgebung**</span><span class="sxs-lookup"><span data-stu-id="13bb6-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bb6-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13bb6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13bb6-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13bb6-117">Der Umgebungsname.</span><span class="sxs-lookup"><span data-stu-id="13bb6-117">The environment name.</span></span> <span data-ttu-id="13bb6-118">Bei einem Ziel eines virtuellen Computers (VM) kann dies der VM-hostname sein.</span><span class="sxs-lookup"><span data-stu-id="13bb6-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="13bb6-119">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="13bb6-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bb6-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13bb6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13bb6-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13bb6-122">Der Name der Farm, zu der das Ziel gehört.</span><span class="sxs-lookup"><span data-stu-id="13bb6-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="13bb6-123">**GUID**</span><span class="sxs-lookup"><span data-stu-id="13bb6-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bb6-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13bb6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13bb6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13bb6-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13bb6-127">Die GUID (sofern vorhanden) des Ziels.</span><span class="sxs-lookup"><span data-stu-id="13bb6-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="13bb6-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="13bb6-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bb6-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13bb6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13bb6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13bb6-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13bb6-132">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="13bb6-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="13bb6-133">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="13bb6-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13bb6-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="13bb6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13bb6-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13bb6-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13bb6-136">Der Name des Ziels.</span><span class="sxs-lookup"><span data-stu-id="13bb6-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="13bb6-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13bb6-137">Examples</span></span>

<span data-ttu-id="13bb6-138">Die folgende Abfrage Zeichenfolge veranschaulicht, wie die Win32- \_ Klasse "sessionbrokertarget" in einer Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13bb6-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="13bb6-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13bb6-139">Requirements</span></span>



| <span data-ttu-id="13bb6-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13bb6-140">Requirement</span></span> | <span data-ttu-id="13bb6-141">Wert</span><span class="sxs-lookup"><span data-stu-id="13bb6-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13bb6-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13bb6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="13bb6-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13bb6-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13bb6-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13bb6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="13bb6-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13bb6-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="13bb6-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="13bb6-146">Namespace</span></span><br/>                | <span data-ttu-id="13bb6-147">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="13bb6-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="13bb6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="13bb6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13bb6-149"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="13bb6-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="13bb6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="13bb6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13bb6-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bb6-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

