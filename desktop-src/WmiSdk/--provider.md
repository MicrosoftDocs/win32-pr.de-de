---
description: Fungiert als übergeordnete Klasse für die \_ \_ Win32Provider-System Klasse.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363520"
---
# <a name="__provider-class"></a><span data-ttu-id="5e3e1-103">\_\_Anbieter Klasse</span><span class="sxs-lookup"><span data-stu-id="5e3e1-103">\_\_Provider class</span></span>

<span data-ttu-id="5e3e1-104">Die **\_ \_ Anbieter** System Klasse ist eine abstrakte Basisklasse, die als übergeordnete Klasse für die [**\_ \_ Win32Provider**](--win32provider.md) -System Klasse fungiert.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="5e3e1-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5e3e1-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e3e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e3e1-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="5e3e1-108">Member</span><span class="sxs-lookup"><span data-stu-id="5e3e1-108">Members</span></span>

<span data-ttu-id="5e3e1-109">Die **\_ \_ Anbieter** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5e3e1-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="5e3e1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e3e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e3e1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e3e1-111">Properties</span></span>

<span data-ttu-id="5e3e1-112">Die **\_ \_ Anbieter** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e3e1-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="5e3e1-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3e1-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5e3e1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e3e1-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5e3e1-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5e3e1-116">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5e3e1-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5e3e1-117">Sprachneutrale Zeichenfolge, die den Anbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="5e3e1-118">Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="5e3e1-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="5e3e1-119">Anbieter \| Version des Anbieters \|</span><span class="sxs-lookup"><span data-stu-id="5e3e1-119">vendor\|provider\|version</span></span>

<span data-ttu-id="5e3e1-120">Der Name des Anbieters steht beispielsweise für Version 1,0 von Microsoft testprovider:</span><span class="sxs-lookup"><span data-stu-id="5e3e1-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="5e3e1-121">"Microsoft \| Test Provider \| v 1.0"</span><span class="sxs-lookup"><span data-stu-id="5e3e1-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e3e1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e3e1-122">Remarks</span></span>

<span data-ttu-id="5e3e1-123">Die **\_ \_ Anbieter** Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="5e3e1-124">Anbieter erstellen [**\_ \_ Win32Provider**](--win32provider.md) -Instanzen, um Informationen über ihre physische Implementierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5e3e1-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3e1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e3e1-125">Requirements</span></span>



| <span data-ttu-id="5e3e1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e3e1-126">Requirement</span></span> | <span data-ttu-id="5e3e1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5e3e1-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5e3e1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e3e1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3e1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e3e1-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5e3e1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e3e1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3e1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e3e1-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5e3e1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e3e1-132">Namespace</span></span><br/>                | <span data-ttu-id="5e3e1-133">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="5e3e1-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5e3e1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e3e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3e1-135">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="5e3e1-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="5e3e1-136">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="5e3e1-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5e3e1-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="5e3e1-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

