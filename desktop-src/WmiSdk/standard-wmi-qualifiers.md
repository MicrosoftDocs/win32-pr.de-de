---
description: Im folgenden werden die für WMI spezifischen Standard Qualifizierer aufgelistet.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: WMI-Standard Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368039"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="a8f6a-103">WMI-Standard Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="a8f6a-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="a8f6a-104">Im folgenden werden die für WMI spezifischen Standard Qualifizierer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="a8f6a-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Trag**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-106">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-106">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-107">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-107">Applies to: classes</span></span>

<span data-ttu-id="a8f6a-108">Gibt an, dass eine Klasse geänderte Qualifizierer enthält, die lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="a8f6a-109">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a8f6a-109">The default is **TRUE**.</span></span>

<span data-ttu-id="a8f6a-110">Die zugeordnete Klasse kann übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-110">The associated class can be translated.</span></span> <span data-ttu-id="a8f6a-111">Um auf die übersetzte Version zuzugreifen, verwenden Sie den Gebiets Schema Bezeichner, um einen Namespace Namen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**\_GetObject umgehen**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-113">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-114">Gilt für: Methoden</span><span class="sxs-lookup"><span data-stu-id="a8f6a-114">Applies to: methods</span></span>

<span data-ttu-id="a8f6a-115">Gibt an, dass der Methodenaufruf direkt an den **ExecMethodAsync** -Aufruf des Anbieters übergeben werden soll, statt an den Anbieter, der zuerst einen Aufruf von **GetObject** zum Überprüfen des Objekt Pfads durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="a8f6a-116">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-116">The default is **FALSE**.</span></span> <span data-ttu-id="a8f6a-117">Die Verwendung von **\_ GetObject umgehen** kann die Leistung erheblich verbessern.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="a8f6a-118">Stellen Sie vor der Verwendung der **Umgehung \_ GetObject** sicher, dass keine der folgenden Aktionen durchgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="a8f6a-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="a8f6a-119">Leiten Sie eine Klasse von der-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="a8f6a-120">Überschreiben Sie die-Methode, die den **\_ GetObject** -Qualifizierer umgeht.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="a8f6a-121">Wenn Sie diese Vorsichtsmaßnahmen nicht befolgen, kann dies dazu führen, dass die Methoden Implementierung der übergeordneten Klasse anstelle der untergeordneten Klasse aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="a8f6a-122">Weitere Informationen finden Sie unter Using the Bypass \_ GetObject Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM- \_ Taste**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-124">Datentyp: **CIM \_ Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="a8f6a-125">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f6a-125">Applies to: properties</span></span>

<span data-ttu-id="a8f6a-126">Gibt an, dass die zugeordnete Eigenschaft eine Schlüsseleigenschaft in CIM, aber nicht in WMI ist.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CimType**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-128">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-129">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f6a-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="a8f6a-130">Enthält Text, der den Typ einer Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-132">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-133">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-133">Applies to: classes</span></span>

<span data-ttu-id="a8f6a-134">Gibt an, dass eine Klasse über Instanzen verfügt, die anderen von einem Anbieter dynamisch bereitgestellten Informationen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Veraltet**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-136">Datentyp: **CIM \_ Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="a8f6a-137">Gilt für: Eigenschaften, Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-137">Applies to: properties, classes</span></span>

<span data-ttu-id="a8f6a-138">Gibt an, dass die Eigenschaft durch eine andere Eigenschaft abgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Ausgestellten**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-140">Gilt für: Klassen, Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f6a-140">Applies to: classes, properties</span></span>

<span data-ttu-id="a8f6a-141">Die **UUID** der zugeordneten-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Schem**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-143">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-144">Gilt für: Klassen, Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f6a-144">Applies to: classes, properties</span></span>

<span data-ttu-id="a8f6a-145">Gibt eine Klasse an, deren Instanzen dynamisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="a8f6a-146">Der Wert dieses Qualifizierers muss auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**Dyn-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-148">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-149">Gilt für: Klassen, Instanzen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-149">Applies to: classes, instances</span></span>

<span data-ttu-id="a8f6a-150">Gibt an, dass eine Instanz Werte enthält, die von dynamischen Eigenschaften Anbietern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="a8f6a-151">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="a8f6a-151">The default is **TRUE**.</span></span>

<span data-ttu-id="a8f6a-152">Sie müssen diesen Qualifizierer für eine solche Instanz angeben.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="a8f6a-153">Nur der Wert " **true** " ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Festen**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-155">Datentyp: **CIM \_ Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="a8f6a-156">Gilt für: Instanzen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-156">Applies to: instances</span></span>

<span data-ttu-id="a8f6a-157">Gibt an, dass der Wert dieser Eigenschaft während der Lebensdauer der Instanz nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-158"><span id="ID"></span><span id="id"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-159">Datentyp: **VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="a8f6a-160">Gilt für: Eigenschaften, Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f6a-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="a8f6a-161">Identifiziert und erstellt eine Eigenschaft oder einen Methoden Parameter eindeutig, wenn MOF-Anweisungen automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="a8f6a-162">Dieser Qualifizierer ist nur für Methoden Parameter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="a8f6a-163">Beim Erstellen von Parametern für eine Methode sollten Klassen-Designer für den ersten Parameter mit der ID (0) beginnen und jede aufeinander folgende Ganzzahl für jeden aufeinander folgenden Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="a8f6a-164">Wenn die **ID** -Qualifizierer versehentlich ausgelassen werden, generiert der MOF-Compiler automatisch **ID** -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Realisierte**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-166">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-166">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-167">Gilt für: Methoden</span><span class="sxs-lookup"><span data-stu-id="a8f6a-167">Applies to: methods</span></span>

<span data-ttu-id="a8f6a-168">Gibt an, dass eine Methode eine Implementierung hat, die von einem Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-170">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-171">Gilt für: Instanzen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-171">Applies to: instances</span></span>

<span data-ttu-id="a8f6a-172">Gibt an, dass eine Instanz Werte enthält, die von einem dynamischen Eigenschaften Anbieter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="a8f6a-173">Der Wert wird als Argument an die [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) -Methode an den Eigenschaften Anbieter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Konfigurations**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-175">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-176">Gilt für: Klassen oder Instanzen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-176">Applies to: classes or instances</span></span>

<span data-ttu-id="a8f6a-177">Gibt die Ursprungssprache für eine Klasse oder eine Instanz an.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="a8f6a-178">Weitere Informationen zu Gebiets Schema Werten finden Sie unter Gebiets Schema [Codes](#locale-codes).</span><span class="sxs-lookup"><span data-stu-id="a8f6a-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**Namespacesecuritysddl**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-180">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-180">Data type: **string array**</span></span>

<span data-ttu-id="a8f6a-181">Gilt für: Namespace Instanzen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-181">Applies to: namespace instances</span></span>

<span data-ttu-id="a8f6a-182">Gibt eine Sicherheits Beschreibung für den Namespace im [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) -Format an.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="a8f6a-183">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6a-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="a8f6a-184">Die SDDL-Zeichenfolge wird von WMI verarbeitet, um die Namespace Sicherheit festzulegen, die jedoch nicht als Zeichenfolge gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="a8f6a-185">Wenn kein Sicherheits Deskriptor angegeben wird, wird die Standard Sicherheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="a8f6a-186">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6a-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optionale**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-188">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-188">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-189">Gilt für: Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f6a-189">Applies to: parameters</span></span>

<span data-ttu-id="a8f6a-190">Gibt an, dass ein Parameter nicht erforderlich ist und dass er über einen gut verhaltenen Standardwert verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-192">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-192">Data type: **string array**</span></span>

<span data-ttu-id="a8f6a-193">Gilt für: Eigenschaften, Methoden</span><span class="sxs-lookup"><span data-stu-id="a8f6a-193">Applies to: properties, methods</span></span>

<span data-ttu-id="a8f6a-194">Ein Satz von Werten, mit denen der Client darüber informiert wird, welche Berechtigungen zum Erstellen von Instanzen, zum Ausfüllen von Eigenschaften oder zum Ausführen von Methoden erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="a8f6a-195">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**Propertycontext**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-197">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-198">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f6a-198">Applies to: properties</span></span>

<span data-ttu-id="a8f6a-199">Gibt an, dass eine Instanzeigenschaft von dynamischen Eigenschafts Anbietern bereitgestellte Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="a8f6a-200">Dieser Qualifizierer muss für eine solche Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="a8f6a-201">Der Wert wird an den Eigenschaften Anbieter als Argument an [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Ab**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-203">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-204">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-204">Applies to: classes</span></span>

<span data-ttu-id="a8f6a-205">Der Wert dieses Qualifizierers ist der Name des dynamischen Anbieters, der Klassen Instanzen bereitstellt und Instanzdaten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="a8f6a-206">Dieser Name muss bei WMI registriert werden, indem eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse mit der **Name** -Eigenschaft erstellt wird, die diesen Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="a8f6a-207">Wenn dieser Qualifizierer für eine Klasse angegeben wird, deren Instanzen dynamisch bereitgestellt werden, muss auch der **dynamische** Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**Requirements-Verschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-209">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-209">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-210">Gilt für: Namespace Instanzen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-210">Applies to: namespace instances</span></span>

<span data-ttu-id="a8f6a-211">Wenn diese Einstellung auf " **true**" festgelegt ist, markiert "Requirements **sencryption** " einen Namespace, sodass Client Anwendungen und Skripts eine Verbindung mit verschlüsselter Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a8f6a-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="a8f6a-212">Die Authentifizierungs Ebene muss in C++ auf **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="a8f6a-213">Bei der Skripterstellung oder Visual Basic muss die Authentifizierungs Ebene auf **wbemauthenticationlevelpktprivacy** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="a8f6a-214">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6a-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="a8f6a-215">Der Qualifizierer wird in [*MOF*](gloss-m.md) mit dem Pragma Namespace Präprozessor-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="a8f6a-216">Weitere Informationen finden Sie unter [Festlegen der Standardprozess-Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md) oder [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a8f6a-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="a8f6a-217">Skript Authentifizierungs Ebenen werden in [**wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)definiert.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-219">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-220">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-220">Applies to: classes</span></span>

<span data-ttu-id="a8f6a-221">Gibt eine Klasse an, die nur über eine Instanz verfügen kann, die keine Schlüsseleigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="a8f6a-222">Nur der Wert **true** (Standard) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Kum**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-224">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-224">Data type: **boolean**</span></span>

<span data-ttu-id="a8f6a-225">Gilt für: Methoden</span><span class="sxs-lookup"><span data-stu-id="a8f6a-225">Applies to: methods</span></span>

<span data-ttu-id="a8f6a-226">Gibt an, ob eine Methode mithilfe der Klassendefinition oder ihrer Instanzen aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="a8f6a-227">Die-Methode kann nicht von einer-Instanz aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-229">Datentyp: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="a8f6a-230">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f6a-230">Applies to: properties</span></span>

<span data-ttu-id="a8f6a-231">Gibt an, dass eine Eigenschaft vom Typ **CIM \_ DateTime** ein Zeitintervall anstelle eines bestimmten Zeitraums darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="a8f6a-232">Um die Eigenschaft als Intervall zu identifizieren, muss der Wert dieses Qualifizierers "Interval" lauten.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="a8f6a-233">Alle anderen Werte für diesen Qualifizierer sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-235">Data type: **string**</span></span>

<span data-ttu-id="a8f6a-236">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-236">Applies to: classes</span></span>

<span data-ttu-id="a8f6a-237">Universell eindeutiger Bezeichner für die Klasse.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**Classversion**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-239">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-239">Data type: **string**</span></span>

<span data-ttu-id="a8f6a-240">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-240">Applies to: classes</span></span>

<span data-ttu-id="a8f6a-241">Die Versionsnummer des-Klassen Objekts.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-241">The version number of the class object.</span></span> <span data-ttu-id="a8f6a-242">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-242">The default is **NULL**.</span></span> <span data-ttu-id="a8f6a-243">Die Versionsnummer wird erhöht, wenn Änderungen an der-Klasse vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="a8f6a-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**Schreibberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="a8f6a-245">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="a8f6a-245">Data type: **string array**</span></span>

<span data-ttu-id="a8f6a-246">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f6a-246">Applies to: properties</span></span>

<span data-ttu-id="a8f6a-247">Ein Satz von Werten, der angibt, welche System Privilegien verfügbar sein müssen und für einen erfolgreichen Schreibvorgang aktiviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8f6a-248">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="a8f6a-249">Gebiets Schema Codes</span><span class="sxs-lookup"><span data-stu-id="a8f6a-249">Locale Codes</span></span>

<span data-ttu-id="a8f6a-250">Ein Gebiets Schema Code hat die Form "MS \_ <Three Digit Language ID> ".</span><span class="sxs-lookup"><span data-stu-id="a8f6a-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="a8f6a-251">Beispielsweise ist das englische Gebiets Schema MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="a8f6a-252">In der folgenden Tabelle werden die Sprach-IDs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="a8f6a-253">Sprache</span><span class="sxs-lookup"><span data-stu-id="a8f6a-253">Language</span></span>              | <span data-ttu-id="a8f6a-254">Sprach-ID (hexadezimal)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="a8f6a-255">Arabisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-255">Arabic</span></span>                | <span data-ttu-id="a8f6a-256">401</span><span class="sxs-lookup"><span data-stu-id="a8f6a-256">401</span></span>                       |
| <span data-ttu-id="a8f6a-257">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="a8f6a-258">416</span><span class="sxs-lookup"><span data-stu-id="a8f6a-258">416</span></span>                       |
| <span data-ttu-id="a8f6a-259">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="a8f6a-260">804</span><span class="sxs-lookup"><span data-stu-id="a8f6a-260">804</span></span>                       |
| <span data-ttu-id="a8f6a-261">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-261">Chinese (Traditional)</span></span> | <span data-ttu-id="a8f6a-262">404</span><span class="sxs-lookup"><span data-stu-id="a8f6a-262">404</span></span>                       |
| <span data-ttu-id="a8f6a-263">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-263">Czech</span></span>                 | <span data-ttu-id="a8f6a-264">405</span><span class="sxs-lookup"><span data-stu-id="a8f6a-264">405</span></span>                       |
| <span data-ttu-id="a8f6a-265">Dänisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-265">Danish</span></span>                | <span data-ttu-id="a8f6a-266">406</span><span class="sxs-lookup"><span data-stu-id="a8f6a-266">406</span></span>                       |
| <span data-ttu-id="a8f6a-267">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-267">Dutch</span></span>                 | <span data-ttu-id="a8f6a-268">413</span><span class="sxs-lookup"><span data-stu-id="a8f6a-268">413</span></span>                       |
| <span data-ttu-id="a8f6a-269">Englisch (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-269">English (default)</span></span>     | <span data-ttu-id="a8f6a-270">409</span><span class="sxs-lookup"><span data-stu-id="a8f6a-270">409</span></span>                       |
| <span data-ttu-id="a8f6a-271">Finnisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-271">Finnish</span></span>               | <span data-ttu-id="a8f6a-272">40 b</span><span class="sxs-lookup"><span data-stu-id="a8f6a-272">40b</span></span>                       |
| <span data-ttu-id="a8f6a-273">Französisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-273">French</span></span>                | <span data-ttu-id="a8f6a-274">40 c</span><span class="sxs-lookup"><span data-stu-id="a8f6a-274">40c</span></span>                       |
| <span data-ttu-id="a8f6a-275">Deutsch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-275">German</span></span>                | <span data-ttu-id="a8f6a-276">407</span><span class="sxs-lookup"><span data-stu-id="a8f6a-276">407</span></span>                       |
| <span data-ttu-id="a8f6a-277">Griechisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-277">Greek</span></span>                 | <span data-ttu-id="a8f6a-278">408</span><span class="sxs-lookup"><span data-stu-id="a8f6a-278">408</span></span>                       |
| <span data-ttu-id="a8f6a-279">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-279">Hebrew</span></span>                | <span data-ttu-id="a8f6a-280">40 d</span><span class="sxs-lookup"><span data-stu-id="a8f6a-280">40d</span></span>                       |
| <span data-ttu-id="a8f6a-281">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-281">Hungarian</span></span>             | <span data-ttu-id="a8f6a-282">40 e</span><span class="sxs-lookup"><span data-stu-id="a8f6a-282">40e</span></span>                       |
| <span data-ttu-id="a8f6a-283">Italienisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-283">Italian</span></span>               | <span data-ttu-id="a8f6a-284">410</span><span class="sxs-lookup"><span data-stu-id="a8f6a-284">410</span></span>                       |
| <span data-ttu-id="a8f6a-285">Japanisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-285">Japanese</span></span>              | <span data-ttu-id="a8f6a-286">411</span><span class="sxs-lookup"><span data-stu-id="a8f6a-286">411</span></span>                       |
| <span data-ttu-id="a8f6a-287">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-287">Korean</span></span>                | <span data-ttu-id="a8f6a-288">412</span><span class="sxs-lookup"><span data-stu-id="a8f6a-288">412</span></span>                       |
| <span data-ttu-id="a8f6a-289">Norwegisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-289">Norwegian</span></span>             | <span data-ttu-id="a8f6a-290">414</span><span class="sxs-lookup"><span data-stu-id="a8f6a-290">414</span></span>                       |
| <span data-ttu-id="a8f6a-291">Polnisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-291">Polish</span></span>                | <span data-ttu-id="a8f6a-292">415</span><span class="sxs-lookup"><span data-stu-id="a8f6a-292">415</span></span>                       |
| <span data-ttu-id="a8f6a-293">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="a8f6a-294">816</span><span class="sxs-lookup"><span data-stu-id="a8f6a-294">816</span></span>                       |
| <span data-ttu-id="a8f6a-295">Russisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-295">Russian</span></span>               | <span data-ttu-id="a8f6a-296">419</span><span class="sxs-lookup"><span data-stu-id="a8f6a-296">419</span></span>                       |
| <span data-ttu-id="a8f6a-297">Spanisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-297">Spanish</span></span>               | <span data-ttu-id="a8f6a-298">c0a</span><span class="sxs-lookup"><span data-stu-id="a8f6a-298">c0a</span></span>                       |
| <span data-ttu-id="a8f6a-299">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-299">Swedish</span></span>               | <span data-ttu-id="a8f6a-300">41d</span><span class="sxs-lookup"><span data-stu-id="a8f6a-300">41D</span></span>                       |
| <span data-ttu-id="a8f6a-301">Türkisch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-301">Turkish</span></span>               | <span data-ttu-id="a8f6a-302">41F</span><span class="sxs-lookup"><span data-stu-id="a8f6a-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="a8f6a-303">Verwenden des " \_ GetObject"-Qualifizierers umgehen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="a8f6a-304">Wenn Sie **den \_ GetObject** -Qualifizierer für eine Methode umgehen, können verwirrende Ergebnisse erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="a8f6a-305">Im folgenden Beispiel werden die **Form** -und **Kreis** Klassen definiert.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="a8f6a-306">Beachten Sie, dass die **Circle** -Klasse von der **Shape** -Klasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="a8f6a-307">Der folgende Befehl von **ExecMethod** verwendet ein **Kreis** Objekt mit dem Namen "mycircle", um einen Kreis zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="a8f6a-308">Im vorherigen Szenario ruft WMI " **GetObject**;" auf. ermittelt, dass "Shape. Name = ' mycircle '" ein **Kreis** ist. und führt die **Zirkel** Implementierung von **drawit** aus.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="a8f6a-309">Wenn Sie jedoch den Qualifizierer " **\_ GetObject umgehen** " für **drawit** verwenden, ruft WMI " **GetObject**" nicht auf, erkennt nicht, dass "Shape. Name = ' mycircle '" ein **Kreis** ist, und führt die **Shape** -Implementierung von **drawit** anstelle der **Circle** -Implementierung von **drawit** aus.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="a8f6a-310">Der folgende Aufruf von **ExecMethod** ruft immer die korrekte Implementierung von **drawit** auf.</span><span class="sxs-lookup"><span data-stu-id="a8f6a-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="a8f6a-311">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8f6a-311">Requirements</span></span>



| <span data-ttu-id="a8f6a-312">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8f6a-312">Requirement</span></span> | <span data-ttu-id="a8f6a-313">Wert</span><span class="sxs-lookup"><span data-stu-id="a8f6a-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a8f6a-314">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-314">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f6a-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8f6a-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a8f6a-316">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8f6a-316">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f6a-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8f6a-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8f6a-318">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8f6a-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f6a-319">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="a8f6a-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="a8f6a-320">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="a8f6a-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="a8f6a-321">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="a8f6a-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

