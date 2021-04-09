---
description: Stellt einen WMI-Namespace dar.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868136"
---
# <a name="__namespace-class"></a><span data-ttu-id="118e2-103">\_\_Namespace-Klasse</span><span class="sxs-lookup"><span data-stu-id="118e2-103">\_\_Namespace class</span></span>

<span data-ttu-id="118e2-104">Die **\_ \_ Namespace** -System Klasse stellt einen WMI-Namespace dar.</span><span class="sxs-lookup"><span data-stu-id="118e2-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="118e2-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="118e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="118e2-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="118e2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="118e2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="118e2-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="118e2-108">Member</span><span class="sxs-lookup"><span data-stu-id="118e2-108">Members</span></span>

<span data-ttu-id="118e2-109">Die **\_ \_ Namespace** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="118e2-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="118e2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="118e2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="118e2-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="118e2-111">Properties</span></span>

<span data-ttu-id="118e2-112">Die **\_ \_ Namespace** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="118e2-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="118e2-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="118e2-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="118e2-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="118e2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="118e2-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="118e2-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="118e2-116">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="118e2-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="118e2-117">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="118e2-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="118e2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="118e2-118">Remarks</span></span>

<span data-ttu-id="118e2-119">Die **\_ \_ Namespace** -Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="118e2-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="118e2-120">Sie können **\_ \_ Namespace** verwenden, um untergeordnete Namespaces innerhalb des aktuellen funktionierenden Namespaces zu identifizieren, zu erstellen und zu löschen, für den Sie ein [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Objekt haben.</span><span class="sxs-lookup"><span data-stu-id="118e2-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="118e2-121">Beim Erstellen einer neuen Instanz des **\_ \_ Namespace** in einem funktionierenden Namespace wird ein untergeordneter Namespace innerhalb des funktionierenden Namespaces erstellt.</span><span class="sxs-lookup"><span data-stu-id="118e2-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="118e2-122">Umgekehrt entfernt das Löschen einer Instanz von **\_ \_ Namespace** den untergeordneten Namespace aus dem funktionierenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="118e2-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="118e2-123">Beachten Sie, dass beim Löschen eines untergeordneten Namespace auch alle seine Klassen und Instanzen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="118e2-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="118e2-124">Durch das Auflisten von Instanzen dieser Klasse in einem funktionierenden Namespace werden die verfügbaren untergeordneten Namespaces bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="118e2-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="118e2-125">Im Stamm \\ Namespace sind z. b. zwei Instanzen von **\_ \_ Namespace**.</span><span class="sxs-lookup"><span data-stu-id="118e2-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="118e2-126">Der **Name** der Eigenschaft ist auf "Default" festgelegt, der andere **Name** ist auf "Cimv2" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="118e2-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="118e2-127">Diese Instanzen stellen die \\ Stamm \\ -Standard \\ \\ Namespaces bzw. root cimv2-Namespaces dar.</span><span class="sxs-lookup"><span data-stu-id="118e2-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="118e2-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="118e2-128">Examples</span></span>

<span data-ttu-id="118e2-129">Das Beispiel zum [Auflisten aller WMI-Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript in der TechNet Gallery verwendet einen rekursiven-Befehl, um alle Instanzen der \_ \_ Namespace Klasse auf einem System aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="118e2-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="118e2-130">Das folgende Codebeispiel ruft alle Namespaces in PowerShell ab.</span><span class="sxs-lookup"><span data-stu-id="118e2-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="118e2-131">Im folgenden Codebeispiel wird das vorherige Beispiel verbessert, und es werden zusätzliche Informationen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="118e2-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="118e2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="118e2-132">Requirements</span></span>



| <span data-ttu-id="118e2-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="118e2-133">Requirement</span></span> | <span data-ttu-id="118e2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="118e2-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="118e2-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="118e2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="118e2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="118e2-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="118e2-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="118e2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="118e2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="118e2-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="118e2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="118e2-139">Namespace</span></span><br/>                | <span data-ttu-id="118e2-140">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="118e2-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="118e2-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="118e2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118e2-142">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="118e2-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="118e2-143">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="118e2-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




