---
title: Win32_SessionBrokerFarm-Klasse
description: Definiert die Abfrage für eine Sitzungs Broker Farm.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarm-Klasse Remotedesktopdienste
- Win32_SessionBrokerFarm Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476695"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="9c6a2-105">Win32- \_ Klasse "sessionbrokerfarm"</span><span class="sxs-lookup"><span data-stu-id="9c6a2-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="9c6a2-106">Definiert die Abfrage für eine Sitzungs Broker Farm.</span><span class="sxs-lookup"><span data-stu-id="9c6a2-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="9c6a2-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c6a2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6a2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c6a2-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="9c6a2-109">Member</span><span class="sxs-lookup"><span data-stu-id="9c6a2-109">Members</span></span>

<span data-ttu-id="9c6a2-110">Die Win32-Klasse " **\_ sessionbrokerfarm** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9c6a2-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="9c6a2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c6a2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c6a2-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c6a2-112">Properties</span></span>

<span data-ttu-id="9c6a2-113">Die Win32-Klasse " **\_ sessionbrokerfarm** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c6a2-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c6a2-114">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="9c6a2-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6a2-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c6a2-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6a2-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c6a2-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6a2-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c6a2-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c6a2-118">Der Name der Sitzungs Broker Farm, die abgefragt werden muss.</span><span class="sxs-lookup"><span data-stu-id="9c6a2-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="9c6a2-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="9c6a2-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c6a2-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c6a2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c6a2-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9c6a2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c6a2-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c6a2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9c6a2-123">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="9c6a2-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9c6a2-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c6a2-124">Examples</span></span>

<span data-ttu-id="9c6a2-125">Die folgende Abfrage Zeichenfolge veranschaulicht, wie die Win32-Klasse " **\_ sessionbrokerfarm** " in einer Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c6a2-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="9c6a2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c6a2-126">Requirements</span></span>



| <span data-ttu-id="9c6a2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c6a2-127">Requirement</span></span> | <span data-ttu-id="9c6a2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9c6a2-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6a2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c6a2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6a2-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9c6a2-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9c6a2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c6a2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6a2-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c6a2-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9c6a2-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c6a2-133">Namespace</span></span><br/>                | <span data-ttu-id="9c6a2-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9c6a2-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9c6a2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9c6a2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c6a2-136"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9c6a2-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c6a2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9c6a2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c6a2-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c6a2-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

