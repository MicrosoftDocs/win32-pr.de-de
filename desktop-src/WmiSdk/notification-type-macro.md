---
description: Das-Benachrichtigungstyp-Makro enthält die folgenden Elemente.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Notification-Type-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356835"
---
# <a name="notification-type-macro"></a><span data-ttu-id="83d09-103">Notification-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="83d09-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="83d09-104">Das-Benachrichtigungstyp-Makro enthält die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="83d09-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="83d09-105">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="83d09-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="83d09-106">Komponenten</span><span class="sxs-lookup"><span data-stu-id="83d09-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="83d09-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Objekt Deskriptor</span><span class="sxs-lookup"><span data-stu-id="83d09-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="83d09-108">Fügt einen Namen an ein SNMP-Ereignis in einem Notification-Type-Makro an.</span><span class="sxs-lookup"><span data-stu-id="83d09-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="83d09-109">In der folgenden Liste werden die Regeln für die Zuordnung des Objekt Deskriptors aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="83d09-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="83d09-110">type</span><span class="sxs-lookup"><span data-stu-id="83d09-110">Type</span></span>                        | <span data-ttu-id="83d09-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="83d09-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d09-112">Gekapselt CIM-Klassenname</span><span class="sxs-lookup"><span data-stu-id="83d09-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="83d09-113">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="83d09-113">"SNMP\_"</span></span><br/> <span data-ttu-id="83d09-114">Name der MIB-Modul Identität</span><span class="sxs-lookup"><span data-stu-id="83d09-114">MIB module identity name</span></span><br/> <span data-ttu-id="83d09-115">Unterstrich ( \_ )</span><span class="sxs-lookup"><span data-stu-id="83d09-115">underscore (\_)</span></span><br/> <span data-ttu-id="83d09-116">Objekt Deskriptor</span><span class="sxs-lookup"><span data-stu-id="83d09-116">object descriptor</span></span><br/> <span data-ttu-id="83d09-117">" \_ Benachrichtigung"</span><span class="sxs-lookup"><span data-stu-id="83d09-117">"\_Notification"</span></span><br/> <span data-ttu-id="83d09-118">Beispiel: die **vtpserverdeaktiviert** -Benachrichtigung von **Cisco-VTP-MIB** wird der **SNMP- \_ Cisco \_ VTP \_ MIB \_ vtpserverdeaktiviert- \_ Benachrichtigung** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="83d09-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="83d09-119">Name der Referenten-CIM-Klasse</span><span class="sxs-lookup"><span data-stu-id="83d09-119">Referent CIM class name</span></span>     | <span data-ttu-id="83d09-120">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="83d09-120">"SNMP\_"</span></span><br/> <span data-ttu-id="83d09-121">Name der MIB-Modul Identität</span><span class="sxs-lookup"><span data-stu-id="83d09-121">MIB module identity name</span></span><br/> <span data-ttu-id="83d09-122">Unterstrich ( \_ )</span><span class="sxs-lookup"><span data-stu-id="83d09-122">underscore (\_)</span></span><br/> <span data-ttu-id="83d09-123">Objekt Deskriptor</span><span class="sxs-lookup"><span data-stu-id="83d09-123">object descriptor</span></span><br/> <span data-ttu-id="83d09-124">" \_ Extendednotification"</span><span class="sxs-lookup"><span data-stu-id="83d09-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="83d09-125">Beispiel: die **vtpserverdeaktiviert** -Benachrichtigung von **Cisco-VTP-MIB** wird **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpserverdeaktiviert \_ extendednotification** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="83d09-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="83d09-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Objects-Klausel</span><span class="sxs-lookup"><span data-stu-id="83d09-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="83d09-127">Listet die Objekte auf, die dem Benachrichtigungs Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="83d09-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="83d09-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Reference-Klausel</span><span class="sxs-lookup"><span data-stu-id="83d09-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="83d09-129">Verweist auf ein anderes Dokument, das weitere Informationen zum-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="83d09-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="83d09-130">Sie wird dem klassenqualifizierungsverweis der CIM-Klasse zugeordnet, der vom Typ Zeichenfolge ist. </span><span class="sxs-lookup"><span data-stu-id="83d09-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="83d09-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Description-Klausel</span><span class="sxs-lookup"><span data-stu-id="83d09-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="83d09-132">Beschreibt das betreffende Objekt.</span><span class="sxs-lookup"><span data-stu-id="83d09-132">Describes the object in question.</span></span> <span data-ttu-id="83d09-133">Es wird der klassenqualifiziererbeschreibung der CIM-Klasse zugeordnet, die vom Typ Zeichenfolge </span><span class="sxs-lookup"><span data-stu-id="83d09-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="83d09-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Status-Klausel</span><span class="sxs-lookup"><span data-stu-id="83d09-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="83d09-135">Gibt an, ob das Objekt unterstützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="83d09-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="83d09-136">Wenn der Status entweder **veraltet** oder **veraltet** ist, wird die Benachrichtigung von der Zuordnung verworfen.</span><span class="sxs-lookup"><span data-stu-id="83d09-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="83d09-137">Andernfalls wird diese Klausel dem gatewayklassenqualifiziererstatus zugeordnet, der vom Typ " **String**" ist. </span><span class="sxs-lookup"><span data-stu-id="83d09-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="83d09-138">Der bevorzugte **Wert für SNMPv1 ist entweder** **obligatorisch** oder **optional**, aber der Qualifizierer kann einen anderen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="83d09-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="83d09-139">Der bevorzugte **Wert für SNMPv2C ist entweder** **Current** oder **veraltet**, aber der Qualifizierer kann einen anderen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="83d09-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83d09-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83d09-140">Remarks</span></span>

<span data-ttu-id="83d09-141">Der SNMP-Anbieter ordnet das **-Benachrichtigungstyp** Makro entweder einer gekapselten oder einer Referenz Klassendefinition zu.</span><span class="sxs-lookup"><span data-stu-id="83d09-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="83d09-142">Eine gekapselte Klassendefinition macht die dem MIB-Objekt zugeordneten Instanzinformationen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83d09-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="83d09-143">Stattdessen codiert die Klassendefinition die Objects-Klausel als eine Reihe von Eigenschaften der CIM-Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="83d09-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="83d09-144">Jede CIM-Eigenschaft gibt den Namen, den Typ und den Wert des entsprechenden MIB-Objekts in der Objects-Klausel wieder.</span><span class="sxs-lookup"><span data-stu-id="83d09-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="83d09-145">Wenn Sie Instanzinformationen benötigen, müssen Sie eine Referenzklasse zuordnen.</span><span class="sxs-lookup"><span data-stu-id="83d09-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="83d09-146">Eine gekapselte Klassendefinition wird der [SnmpNotification](snmpnotification.md) -Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="83d09-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="83d09-147">Eine Referenten Klasse definiert ein MIB-Objekt und die Instanzinformationen, die zum Abrufen des Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83d09-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="83d09-148">Die Klassendefinition codiert die Objects-Klausel als eine Reihe von Eigenschaften der CIM-Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="83d09-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="83d09-149">Jede CIM-Eigenschaft gibt den Namen des entsprechenden MIB-Objekts in der Objects-Klausel und den Typ als eingebettetes Objekt wieder, das eine Instanz der diesem MIB-Objekt zugeordneten Klasse wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="83d09-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="83d09-150">Der Anbieter generiert dann eine Klasse, die mit dem MIB-Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="83d09-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="83d09-151">**Ifindex** wird z. b. einer eingebetteten Klasse mit dem Namen **SNMP \_ RFC1213 \_ MIB \_ ifindex** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="83d09-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="83d09-152">Weitere Informationen zu diesem Klassentyp finden Sie unter [Object-Type-Makro](object-type-macro.md).</span><span class="sxs-lookup"><span data-stu-id="83d09-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




