---
description: Enthält die Sicherheitsrechte für den Namespace in Form einer Sicherheits Beschreibung.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368967"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="d329d-103">\_\_thisNamespace-Klasse</span><span class="sxs-lookup"><span data-stu-id="d329d-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="d329d-104">Die **\_ \_ thisNamespace** -System Klasse enthält die Sicherheitsrechte für den-Namespace in Form einer Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="d329d-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="d329d-105">Diese Klasse und eine einzelne Instanz befinden sich in allen Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d329d-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="d329d-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d329d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d329d-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d329d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d329d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d329d-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="d329d-109">Member</span><span class="sxs-lookup"><span data-stu-id="d329d-109">Members</span></span>

<span data-ttu-id="d329d-110">Die **\_ \_ thisNamespace** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d329d-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="d329d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d329d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d329d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d329d-112">Properties</span></span>

<span data-ttu-id="d329d-113">Die **\_ \_ thisNamespace** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d329d-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d329d-114">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d329d-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d329d-115">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="d329d-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d329d-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d329d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d329d-117">Der Sicherheits Deskriptor, der beschreibt, wer auf den Namespace zugreifen kann und wer in den Namespace lesen oder in diesen schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="d329d-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="d329d-118">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d329d-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="d329d-119">Weitere Informationen zum Format von Sicherheits Deskriptoren finden Sie unter [Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors) im Abschnitt "Sicherheit" des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d329d-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d329d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d329d-120">Remarks</span></span>

<span data-ttu-id="d329d-121">Die Singleton-Instanz von **\_ \_ thisNamespace** ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d329d-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="d329d-122">Verwenden Sie die Methoden der [**\_ \_ SystemSecurity**](--systemsecurity.md) -Klasse, um die Einstellungen der sicherheitsbeschreibungenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d329d-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="d329d-123">Die **\_ \_ thisNamespace** -Klasse wird von [**\_ \_ System Class**](--systemclass.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d329d-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d329d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d329d-124">Requirements</span></span>



| <span data-ttu-id="d329d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d329d-125">Requirement</span></span> | <span data-ttu-id="d329d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d329d-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d329d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d329d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d329d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d329d-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d329d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d329d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d329d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d329d-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d329d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d329d-131">Namespace</span></span><br/>                | <span data-ttu-id="d329d-132">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="d329d-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d329d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d329d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d329d-134">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="d329d-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="d329d-135">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="d329d-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

