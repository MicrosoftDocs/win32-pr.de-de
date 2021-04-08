---
description: Die \_ WMI-Klasse "Win32 shareesdirectory Association" verknüpft eine freigegebene Ressource auf dem Computersystem und das Verzeichnis, dem Sie zugeordnet ist.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747824"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="fc3b6-103">Win32 \_ sharededirectory-Klasse</span><span class="sxs-lookup"><span data-stu-id="fc3b6-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="fc3b6-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ shareesdirectory** Association" verknüpft eine freigegebene Ressource auf dem Computersystem und das Verzeichnis, dem Sie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fc3b6-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="fc3b6-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc3b6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fc3b6-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="fc3b6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3b6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc3b6-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="fc3b6-108">Member</span><span class="sxs-lookup"><span data-stu-id="fc3b6-108">Members</span></span>

<span data-ttu-id="fc3b6-109">Die **Win32 \_ sharetodirectory** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fc3b6-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="fc3b6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc3b6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc3b6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc3b6-111">Properties</span></span>

<span data-ttu-id="fc3b6-112">Die **Win32 \_ sharededirectory** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc3b6-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc3b6-113">**Teilen**</span><span class="sxs-lookup"><span data-stu-id="fc3b6-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc3b6-114">Datentyp: **Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="fc3b6-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="fc3b6-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc3b6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc3b6-116">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI- \| Win32- \_ Freigabe")</span><span class="sxs-lookup"><span data-stu-id="fc3b6-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="fc3b6-117">Verweis auf die-Instanz, die die Eigenschaften einer freigegebenen Ressource darstellt, die über das Verzeichnis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fc3b6-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="fc3b6-118">**Sharedelta**</span><span class="sxs-lookup"><span data-stu-id="fc3b6-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc3b6-119">Datentyp: **CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="fc3b6-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="fc3b6-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc3b6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc3b6-121">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM- \_ Verzeichnis")</span><span class="sxs-lookup"><span data-stu-id="fc3b6-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="fc3b6-122">Verweis auf die-Instanz, die die Eigenschaften des Verzeichnisses darstellt, das einer freigegebenen Ressource zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="fc3b6-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc3b6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc3b6-123">Requirements</span></span>



| <span data-ttu-id="fc3b6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc3b6-124">Requirement</span></span> | <span data-ttu-id="fc3b6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fc3b6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3b6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc3b6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3b6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc3b6-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc3b6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc3b6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3b6-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc3b6-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc3b6-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc3b6-130">Namespace</span></span><br/>                | <span data-ttu-id="fc3b6-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fc3b6-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc3b6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fc3b6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc3b6-133"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fc3b6-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc3b6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fc3b6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc3b6-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc3b6-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc3b6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc3b6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3b6-137">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="fc3b6-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
