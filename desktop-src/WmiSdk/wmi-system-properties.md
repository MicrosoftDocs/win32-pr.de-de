---
description: Windows-Verwaltungsinstrumentation (WMI) definiert eine Gruppe von Systemeigenschaften, die allen Klassen und Klassen Instanzen zugeordnet sind.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: WMI-System Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215441"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="3e070-103">WMI-System Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e070-103">WMI System Properties</span></span>

<span data-ttu-id="3e070-104">Windows-Verwaltungsinstrumentation (WMI) definiert eine Gruppe von Systemeigenschaften, die allen Klassen und Klassen Instanzen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3e070-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="3e070-105">Wie bei System Klassen beginnen System Eigenschaftsnamen mit einem doppelten Unterstrich und unterscheiden sich von Eigenschaften, die von Anwendungen oder Anbietern erstellt werden, die nicht mit einem einzelnen oder einem doppelten Unterstrich beginnen dürfen.</span><span class="sxs-lookup"><span data-stu-id="3e070-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="3e070-106">Eine andere Möglichkeit, eine System Eigenschaft zu identifizieren, ist die Verwendung der [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3e070-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="3e070-107">System Eigenschaften sind jederzeit verfügbar, Werte sind jedoch möglicherweise **null**.</span><span class="sxs-lookup"><span data-stu-id="3e070-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="3e070-108">**Null** gibt an, dass eine Eigenschaft nicht für ein bestimmtes Objekt gilt.</span><span class="sxs-lookup"><span data-stu-id="3e070-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="3e070-109">Systemeigenschaften sind jedoch möglicherweise nicht immer für alle Klassen oder Instanzen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e070-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="3e070-110">Systemeigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e070-110">System Properties</span></span>

<span data-ttu-id="3e070-111">In der folgenden Liste werden die WMI-Systemeigenschaften beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3e070-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="3e070-112">Die angegebenen Beispiele stammen aus den Systemeigenschaften der [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse, die unten in diesem Thema beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3e070-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="3e070-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Klassi**</span><span class="sxs-lookup"><span data-stu-id="3e070-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-114">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-115">Zugriffstyp: schreibgeschützt für Instanzen; Lese-/Schreibzugriff für Klassen</span><span class="sxs-lookup"><span data-stu-id="3e070-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="3e070-116">Der Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="3e070-116">The name of the class.</span></span>

<span data-ttu-id="3e070-117">Beispiel: Win32 \_ optionalfeature</span><span class="sxs-lookup"><span data-stu-id="3e070-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="3e070-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Ableitung**</span><span class="sxs-lookup"><span data-stu-id="3e070-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-119">Datentyp: **CIM- \_ Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3e070-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="3e070-120">Zugriffstyp: schreibgeschützt sowohl für Instanzen als auch für Klassen</span><span class="sxs-lookup"><span data-stu-id="3e070-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="3e070-121">Klassenhierarchie der aktuellen Klasse oder Instanz.</span><span class="sxs-lookup"><span data-stu-id="3e070-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="3e070-122">Das erste Element ist die unmittelbar übergeordnete Klasse, das nächste ist das übergeordnete Element, usw. das letzte Element ist die Basisklasse.</span><span class="sxs-lookup"><span data-stu-id="3e070-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="3e070-123">Beispiel: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}</span><span class="sxs-lookup"><span data-stu-id="3e070-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="3e070-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Els**</span><span class="sxs-lookup"><span data-stu-id="3e070-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-125">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-126">Access type: Read-only</span></span>

<span data-ttu-id="3e070-127">Der Name der Klasse der obersten Ebene, von der die Klasse oder Instanz abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3e070-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="3e070-128">Wenn diese Klasse oder Instanz die Klasse der obersten Ebene ist, sind die Werte von " **\_ \_ Dynastie** " und " **\_ \_ Class** " identisch.</span><span class="sxs-lookup"><span data-stu-id="3e070-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="3e070-129">Beispiel: CIM \_ ManagedSystemElement</span><span class="sxs-lookup"><span data-stu-id="3e070-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="3e070-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Umgeleitet**</span><span class="sxs-lookup"><span data-stu-id="3e070-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-131">Datentyp: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="3e070-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="3e070-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-132">Access type: Read-only</span></span>

<span data-ttu-id="3e070-133">Der Wert, der verwendet wird, um zwischen Klassen und Instanzen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="3e070-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="3e070-134">Dieser Wert ist die **WBEM- \_ \_ Klasse Class** (1) für Klassen und die **WBEM- \_ \_ Typinstanz** (2) für-Instanzen und-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="3e070-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="3e070-135">Beispiel: 2</span><span class="sxs-lookup"><span data-stu-id="3e070-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="3e070-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e070-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="3e070-137">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-138">Access type: Read-only</span></span>

<span data-ttu-id="3e070-139">Der Name des [*Namespace*](gloss-n.md) der Klasse oder Instanz.</span><span class="sxs-lookup"><span data-stu-id="3e070-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="3e070-140">Beispiel: root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3e070-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="3e070-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_ADS**</span><span class="sxs-lookup"><span data-stu-id="3e070-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-142">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-143">Access type: Read-only</span></span>

<span data-ttu-id="3e070-144">Vollständiger Pfad zur Klasse oder Instanz – einschließlich Server und Namespace.</span><span class="sxs-lookup"><span data-stu-id="3e070-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="3e070-145">Beispiel: \\ \\ myserver \\ root \\ CIMV2: Win32 \_ optionalfeature. Name = "Telnetclient"</span><span class="sxs-lookup"><span data-stu-id="3e070-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="3e070-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Anzahl von Eigenschaften \_**</span><span class="sxs-lookup"><span data-stu-id="3e070-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-147">Datentyp: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="3e070-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="3e070-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-148">Access type: Read-only</span></span>

<span data-ttu-id="3e070-149">Anzahl der nicht-Systemeigenschaften, die für die Klasse oder Instanz definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3e070-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="3e070-150">Beispiel: 6</span><span class="sxs-lookup"><span data-stu-id="3e070-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="3e070-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_RelPath**</span><span class="sxs-lookup"><span data-stu-id="3e070-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-152">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-153">Access type: Read-only</span></span>

<span data-ttu-id="3e070-154">Relativer Pfad zur-Klasse oder-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3e070-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="3e070-155">Beispiel: Win32 \_ optionalfeature. Name = "Telnetclient"</span><span class="sxs-lookup"><span data-stu-id="3e070-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="3e070-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servers**</span><span class="sxs-lookup"><span data-stu-id="3e070-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-157">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-158">Access type: Read-only</span></span>

<span data-ttu-id="3e070-159">Der Name des Servers, der die Klasse oder Instanz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3e070-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="3e070-160">Beispiel: MyServer</span><span class="sxs-lookup"><span data-stu-id="3e070-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="3e070-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Übergeordneten Klasse**</span><span class="sxs-lookup"><span data-stu-id="3e070-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="3e070-162">Datentyp: **CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e070-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="3e070-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3e070-163">Access type: Read-only</span></span>

<span data-ttu-id="3e070-164">Der Name der unmittelbaren übergeordneten Klasse der Klasse oder Instanz.</span><span class="sxs-lookup"><span data-stu-id="3e070-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="3e070-165">Beispiel: CIM \_ LogicalElement</span><span class="sxs-lookup"><span data-stu-id="3e070-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="3e070-166">Mit dem folgenden PowerShell-Code werden die Eigenschaften der [**Win32- \_ Funktion "optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) " abgerufen, die die Systemeigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="3e070-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="3e070-167">Im vorherigen Codebeispiel wird Folgendes zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="3e070-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
