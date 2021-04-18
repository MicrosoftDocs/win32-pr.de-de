---
description: Eine konkrete Superklasse für CIM-Warn Benachrichtigungen.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: CIM_AlertIndication-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345647"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="cb5d4-103">CIM- \_ alertindikation-Klasse</span><span class="sxs-lookup"><span data-stu-id="cb5d4-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="cb5d4-104">Eine konkrete Superklasse für CIM-Warn Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="cb5d4-105">**CIM \_ Alertindikation** ist eine spezialisierte Art von **CIM \_** -anverweisklasse, die Informationen über den Schweregrad, die Ursache, Empfohlene Aktionen und andere Daten für ein reales Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="cb5d4-106">Dieses Ereignis und seine Daten können auch in der CIM-Klassenhierarchie modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb5d4-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="cb5d4-108">Member</span><span class="sxs-lookup"><span data-stu-id="cb5d4-108">Members</span></span>

<span data-ttu-id="cb5d4-109">Die **CIM \_ alertindikation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cb5d4-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="cb5d4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb5d4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb5d4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb5d4-111">Properties</span></span>

<span data-ttu-id="cb5d4-112">Die **CIM \_ alertindikation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb5d4-113">**Alertingelementformat**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-116">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Alertingmanagedelta**","**CIM \_ alertindikation**.**Otheralertingelementformat**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-117">Das Format der **alertingmanagedelta** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb5d4-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-119">Das Format ist unbekannt oder kann von einer CIM-Client Anwendung nicht sinnvoll interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb5d4-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-121">Das Format wird durch den Wert der otheralertingelementformat-Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="cb5d4-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Cifibjectpath** (2)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-123">Das Format ist ein ciwbjectpath, der eine Instanz im CIM-Schema angibt.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb5d4-124">**Alertingmanagedelta**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-127">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Alertingelementformat**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-128">Die identifizierenden Informationen der Entität (d. h. der Instanz), für die diese Angabe generiert wird.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="cb5d4-129">Die-Eigenschaft enthält den Pfad einer Instanz, die als Zeichen folgen Parameter codiert ist, wenn die Instanz im CIM-Schema modelliert ist.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="cb5d4-130">Wenn es sich nicht um eine CIM-Instanz handelt, enthält die Eigenschaft eine Identifikations Zeichenfolge, die die Entität benennt, für die die Warnung generiert wurde</span><span class="sxs-lookup"><span data-stu-id="cb5d4-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="cb5d4-131">Der Pfad oder die identifizierende Zeichenfolge wird gemäß der alertingelementformat-Eigenschaft formatiert.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-135">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Ereignistyp ")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-136">Die primäre Klassifizierung des Hinweises.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb5d4-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-138">\- Außer.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-138">\- Other.</span></span> <span data-ttu-id="cb5d4-139">Die otheralerttype-Eigenschaft des Hinweises überträgt die Klassifizierung.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="cb5d4-140">Die Verwendung von "Other" in einer Enumeration ist eine Standard-CIM-Konvention.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="cb5d4-141">Dies bedeutet, dass die aktuelle Angabe nicht in die von dieser Enumeration beschriebenen Kategorien passt.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="cb5d4-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Kommunikations Warnung** (2)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-143">Eine Angabe dieses Typs ist hauptsächlich mit den Prozeduren und/oder Prozessen verknüpft, die erforderlich sind, um Informationen von einem Punkt an einen anderen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="cb5d4-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Warnung** (3)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-145">Eine Angabe dieses Typs ist in erster Linie mit einer Verschlechterung oder Fehlern in der Leistung oder Funktion einer Entität verknüpft.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="cb5d4-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Verarbeitungsfehler** (4)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-147">Eine Angabe dieses Typs ist hauptsächlich mit einem Software-oder Verarbeitungsfehler verknüpft.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="cb5d4-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Geräte Warnung** (5)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-149">Eine Angabe dieses Typs ist hauptsächlich mit einem Geräte-oder Hardwarefehler verknüpft.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="cb5d4-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Umwelt Warnung** (6)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-151">Umwelt Warnung.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-151">Environmental Alert.</span></span> <span data-ttu-id="cb5d4-152">Eine Angabe dieses Typs ist hauptsächlich einer Bedingung zugeordnet, die sich auf ein Gehäuse bezieht, in dem sich die Hardware befindet, oder auf andere Umgebungs Aspekte.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="cb5d4-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Modell Änderung** (7)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-154">Die Angabe behandelt Änderungen im Informationsmodell.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="cb5d4-155">Beispielsweise kann eine Lebenszyklus Anzeige einbettet werden, um zu übermitteln, welche spezifischen Modelländerungen gewarnt werden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="cb5d4-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Sicherheitswarnung** (8)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-157">.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-157">.</span></span> <span data-ttu-id="cb5d4-158">Eine Angabe dieses Typs ist zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb5d4-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-162">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Zusätzlicher Text ")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-163">Eine kurze Beschreibung des Hinweises.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-164">**EventID**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-167">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Probableursache**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-168">Ein Instrumentierungs-oder Anbieter spezifischer Wert, der das zugrunde liegende reale Ereignis beschreibt, das durch die Anzeige dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="cb5d4-169">Hinweise mit dem gleichen **EventID** -Wert ungleich NULL werden von der Erstellungs Entität in Erwägung gezogen, um das gleiche Ereignis darzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="cb5d4-170">Der Vergleich zweier **EventID-** Werte wird nur für Warnhinweise mit identischen, nicht-NULL-Werten der Eigenschaften **systemkreateclassname**, **Systemname** und **providerName** definiert.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-172">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-174">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Probableursache**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-175">Die Uhrzeit und das Datum, das angibt, wann das zugrunde liegende Ereignis erstmals erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="cb5d4-176">Wenn diese Werte angegeben werden und die erstellende Entität diese Informationen nicht bereitstellen kann, muss diese Eigenschaft auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="cb5d4-177">Dieser Wert basiert auf dem Konzept des lokalen Datums und der Ortszeit des CIM- **\_ managesystemelement** -Objekts, das die Angabe generiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-178">**Meldung**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-181">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**MessageId**","**CIM \_ alertdeutet**.**Messagearguments**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-182">Die formatierte Meldung für den Warnungs Hinweis.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="cb5d4-183">Diese Meldung wird formatiert, indem mindestens ein dynamisches Element, das in der **messagearguments** -Eigenschaft angegeben ist, und die statischen Elemente, die durch die **MessageId** -Eigenschaft eindeutig identifiziert werden, kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-184">**Messagearguments**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-185">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cb5d4-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-187">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Meldung**","**CIM \_ alertindikation**.**MessageId**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-188">Ein Array, das den dynamischen Inhalt der Meldung für die Warnungs Anzeige enthält.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-189">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-192">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Meldung**","**CIM \_ alertindikation**.**Messagearguments**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-193">Die eindeutige ID des Nachrichten Formats, die den Gültigkeitsbereich der in **owningentity** angegebenen Organisation wider gibt.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-194">**Otheralertingelementformat**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-197">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Alertingelementformat**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-198">Definiert das Format der **alertingmanagedelta ement** -Eigenschaft, wenn die **alertingelementformat** -Eigenschaft auf "1" (sonstige) festgelegt ist. Andernfalls muss dieser Wert auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-199">**Otheralerttype**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-202">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Alerttype**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-203">Eine Zeichenfolge, die den **alerttype** -Wert beschreibt, wenn die **alerttype** -Eigenschaft auf "1" (sonstige Zustandsänderung) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-204">**Owningentity**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-207">Die eindeutige ID der Organisation, die Besitzer der Definition des Formats der **Message** -Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="cb5d4-208">**Owningentity** muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder eindeutigen Namen enthalten, der im Besitz der Geschäfts Entität oder des Standard Texts ist, die das Nachrichtenformat definiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-209">**Wahrnehmgrad**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-210">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-212">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("wahrvedschwere Grad"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Wahrgenommene Schweregrade ")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-213">Der Schweregrad der Warnungs Angabe aus der Sicht des Elements, das die Warnung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb5d4-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-215">Folgt der allgemeinen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb5d4-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-217">Gibt an, dass der Wert des schwere Grads in der Eigenschaft otherschwere Grad gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="cb5d4-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-219">Folgt der allgemeinen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="cb5d4-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>Heruntergestuft **/Warnung** (3)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-221">Sollte verwendet werden, wenn der Benutzer die Entscheidung treffen soll, ob eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="cb5d4-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Neben** Version (4)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-223">Gibt an, dass eine Aktion erforderlich ist, aber die Situation zu diesem Zeitpunkt nicht schwerwiegend ist.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="cb5d4-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Haupt** Version (5)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-225">Gibt an, dass jetzt eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="cb5d4-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (6)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-227">Jetzt ist eine Aktion erforderlich, und der Bereich ist umfangreich (möglicherweise kommt es zu einem bevorstehenden Ausfall einer wichtigen Ressource).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="cb5d4-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>Schwerwiegend **/nicht wiederherstellbar** (7)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cb5d4-229">Gibt an, dass ein Fehler aufgetreten ist, aber zu spät ist, um Abhilfemaßnahmen zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cb5d4-230">**Probableursache**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-231">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-233">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Wahrscheinliche Ursache "," Empfehlung. ITU \| M3100. probablecause "," ITU-IANA-Wecker-TC "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Probablecaueindescription**","**CIM \_ alertindikation**.**EventID**","**CIM \_ alertindikation**.**EventTime**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-234">Die wahrscheinliche Ursache der Situation, die zu der Warnungs Warnung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb5d4-235">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb5d4-236">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="cb5d4-237">**Adapter-/Kartenfehler** (2)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="cb5d4-238">**Fehler des Anwendungs Subsystems** (3)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="cb5d4-239">**Reduzierte Bandbreite** (4)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="cb5d4-240">**Fehler bei der Verbindungs Herstellung** (5)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="cb5d4-241">**Kommunikationsprotokoll Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="cb5d4-242">**Kommunikations Subsystem-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="cb5d4-243">**Konfigurations-/Anpassungsfehler** (8)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="cb5d4-244">**Überlastung** (9)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="cb5d4-245">Beschädigte **Daten** (10)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="cb5d4-246">**Limit für CPU-Zyklen überschritten** (11)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="cb5d4-247">**DataSet/Modem-Fehler** (12)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="cb5d4-248">Herunter gestufter **Signal** (13)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="cb5d4-249">**DTE-DCE-Schnittstellen Fehler** (14)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="cb5d4-250">**Gehäuse Tür geöffnet** (15)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="cb5d4-251">**Geräte** Fehler (16)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="cb5d4-252">**Übermäßige Vibrationen** (17)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="cb5d4-253">**Datei Format Fehler** (18)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="cb5d4-254">**Feuer erkannt** (19)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="cb5d4-255">Über **Flutung erkannt** (20)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="cb5d4-256">**Rahmen Fehler** (21)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="cb5d4-257">**HVAC-Problem** (22)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="cb5d4-258">**Feuchtigkeit nicht akzeptabel** (23)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="cb5d4-259">E **/a-Gerätefehler** (24)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="cb5d4-260">**Eingabegeräte Fehler** (25)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="cb5d4-261">**LAN-Fehler** (26)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="cb5d4-262">Es wurde ein **nicht giftiger Leck erkannt** (27)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="cb5d4-263">**Fehler beim übertragen lokaler Knoten** (28)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="cb5d4-264">**Verlust von Frame** (29)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="cb5d4-265">**Verlust von Signal** (30)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="cb5d4-266">**Material Versorgung erschöpft** (31)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="cb5d4-267">**Multiplexer-Problem** (32)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="cb5d4-268">**Nicht** genügend Arbeitsspeicher (33)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="cb5d4-269">**Ausgabegeräte Fehler** (34)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="cb5d4-270">Beeinträchtigung der **Leistung** (35)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="cb5d4-271">**Energie Problem** (36)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="cb5d4-272">**Unzulässiger Druck** (37)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="cb5d4-273">**Prozessor Problem (interner Computerfehler)** (38)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="cb5d4-274">**Pump Fehler** (39)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="cb5d4-275">**Warteschlangen Größe überschritten** (40)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="cb5d4-276">**Empfangs Fehler** (41)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="cb5d4-277">**Empfänger Fehler** (42)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="cb5d4-278">**Remote Knoten-Übertragungsfehler** (43)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="cb5d4-279">**Ressource mit oder fast der Kapazität** (44)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="cb5d4-280">**Antwortzeit übertrieben** (45)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="cb5d4-281">**Datenübertragungs Rate übermäßig** hoch (46)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="cb5d4-282">**Software Fehler** (47)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="cb5d4-283">Das **Software Programm wurde abgebrochen** (48).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="cb5d4-284">**Software Programmfehler (falsche Ergebnisse)** (49)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="cb5d4-285">**Speicher Kapazitäts Problem** (50)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="cb5d4-286">**Temperatur unzulässig** (51)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="cb5d4-287">**Schwellenwert überschritten** (52)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="cb5d4-288">**Zeit Steuerungs Problem** (53)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="cb5d4-289">Es wurde ein **giftiger Leck erkannt** (54)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="cb5d4-290">**Übertragungsfehler** (55)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="cb5d4-291">Übertragungs **Fehler** (56)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="cb5d4-292">**Zugrunde liegende Ressource nicht verfügbar** (57)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="cb5d4-293">**Versions** Konflikt (58)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="cb5d4-294">**Vorherige Warnung gelöscht** (59)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="cb5d4-295">**Anmeldeversuche fehlgeschlagen** (60)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="cb5d4-296">**Software Viren erkannt** (61)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="cb5d4-297">**Hardware Sicherheits** Verletzung (62)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="cb5d4-298">**Denial-of-Service erkannt** (63)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="cb5d4-299">Nicht übereinstimmende **Sicherheits** Anmelde Informationen (64)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="cb5d4-300">Nicht **autorisierter Zugriff** (65)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="cb5d4-301">**Alarm empfangen** (66)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="cb5d4-302">**Verlust des Zeigers** (67)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="cb5d4-303">**Nutzlast nicht überein** Stimmungen (68)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="cb5d4-304">**Übertragungsfehler** (69)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="cb5d4-305">**Übermäßige Fehler Rate** (70)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="cb5d4-306">Ablauf **Verfolgungs Problem** (71)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="cb5d4-307">**Element nicht verfügbar** (72)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="cb5d4-308">Das **Element fehlt** (73).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="cb5d4-309">**Verlust von Multiframe** (74)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="cb5d4-310">**Übertragungskanal Fehler** (75)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="cb5d4-311">**Ungültige Nachricht empfangen** (76)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="cb5d4-312">**Routing Fehler** (77)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="cb5d4-313">**Backplane-Fehler** (78)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="cb5d4-314">**Bezeichnerduplizierung** (79)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="cb5d4-315">**Fehler beim Schutz Pfad** (80).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="cb5d4-316">**Synchronisierungs Verlust oder nicht überein** stimmende (81)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="cb5d4-317">**Terminal Problem** (82)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="cb5d4-318">**Echt Zeit Taktfehler** (83)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="cb5d4-319">**Antennen Fehler** (84)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="cb5d4-320">**Akku Ladefehler** (85)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="cb5d4-321">Datenträger **Fehler** (86)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="cb5d4-322">**Frequency Spring failure-Fehler** (87)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="cb5d4-323">**Verlust der Redundanz** (88)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="cb5d4-324">**Stromversorgung-Fehler** (89)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="cb5d4-325">**Signal Qualitäts Problem** (90)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="cb5d4-326">**Akku Entladung** (91)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="cb5d4-327">**Akku Fehler** (92)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="cb5d4-328">**Kommerzielles Energie Problem** (93)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="cb5d4-329">**Lüfterfehler** (94)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="cb5d4-330">**Engine-Fehler** (95)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="cb5d4-331">**Sensor Fehler** (96)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="cb5d4-332">**Fuse-Fehler** (97)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="cb5d4-333">**Generator Fehler** (98)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="cb5d4-334">**Niedrige Akku** Kapazität (99)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="cb5d4-335">**Niedriges Benzin** (100)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="cb5d4-336">**Niedriges Wasser** (101)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="cb5d4-337">**Explosiver Gas** (102)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="cb5d4-338">**Hohe Wind** Vorgänge (103)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="cb5d4-339">**Ice-BUILDUP** (104)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="cb5d4-340">**Rauch** (105)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="cb5d4-341">Arbeits **Speicher stimmt nicht überein** (106).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="cb5d4-342">**Nicht genügend CPU-Zyklen** (107)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="cb5d4-343">**Software Umgebungs Problem** (108)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="cb5d4-344">**Fehler beim Software Download** (109).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="cb5d4-345">Das **Element wurde erneut initialisiert** (110).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="cb5d4-346">**Timeout** (111)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="cb5d4-347">**Protokollierungs Probleme** (112)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="cb5d4-348">Der **Leck wurde erkannt** (113).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="cb5d4-349">**Fehler beim Schutzmechanismus** (114).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="cb5d4-350">**Schützen von Ressourcen Fehlern** (115)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="cb5d4-351">**Daten Bank Inkonsistenz** (116)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="cb5d4-352">**Authentifizierungsfehler** (117)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="cb5d4-353">**Verletzung der Vertraulichkeit** (118)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="cb5d4-354">**Kabel Manipulations** Funktion (119)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="cb5d4-355">**Verzögerte Informationen** (120)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="cb5d4-356">**Doppelte Informationen** (121)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="cb5d4-357">**Fehlende Informationen** (122)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="cb5d4-358">**Informations Änderung** (123)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="cb5d4-359">**Informationen außerhalb der Reihenfolge** (124)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="cb5d4-360">Der **Schlüssel ist abgelaufen** (125).</span><span class="sxs-lookup"><span data-stu-id="cb5d4-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="cb5d4-361">**Nicht abstreitbare Fehler** (126)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="cb5d4-362">**Aktivität außerhalb der Stunden** (127)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="cb5d4-363">**Out-of-Service** (128)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="cb5d4-364">**Verfahrensfehler** (129)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="cb5d4-365">**Unerwartete Informationen** (130)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb5d4-366">**Probablecauendescription**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-369">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ alertindikation**".**Probableursache**")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-370">Zusätzliche Informationen, die sich auf die **probablecause** -Eigenschaft beziehen.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-372">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-374">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-375">Der Name des Anbieters, der die Angabe generiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-376">**Empfehlungs Aktionen**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-377">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cb5d4-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-379">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Vorgeschlagene Reparatur Aktionen ")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-380">Frei Form Beschreibungen der empfohlenen Maßnahmen zur Behebung der Ursache der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-381">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-384">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-385">Der Wert von " **kreationclassname** " des Bereichs Systems für den Anbieter, der die Angabe generiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-386">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-389">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-390">Der Name des Bereichs Systems für den Anbieter, der die Angabe generiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="cb5d4-391">**Populär**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb5d4-392">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb5d4-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb5d4-394">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Trend-")</span><span class="sxs-lookup"><span data-stu-id="cb5d4-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="cb5d4-395">Bietet Informationen zu Trends, die sich in der Trend-und abwärts skalieren oder ohne Änderungen befinden.</span><span class="sxs-lookup"><span data-stu-id="cb5d4-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb5d4-396">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cb5d4-397">**Nicht zutreffend** (1)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="cb5d4-398">**Trend aufwärts** (2)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="cb5d4-399">**Trend nach unten** (3)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="cb5d4-400">**Keine Änderung** (4)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-400">**No Change** (4)</span></span>


<span data-ttu-id="cb5d4-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cb5d4-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cb5d4-402">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb5d4-402">Requirements</span></span>



| <span data-ttu-id="cb5d4-403">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb5d4-403">Requirement</span></span> | <span data-ttu-id="cb5d4-404">Wert</span><span class="sxs-lookup"><span data-stu-id="cb5d4-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5d4-405">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-405">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5d4-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cb5d4-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cb5d4-407">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb5d4-407">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5d4-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cb5d4-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cb5d4-409">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb5d4-409">Namespace</span></span><br/>                | <span data-ttu-id="cb5d4-410">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cb5d4-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cb5d4-411">MOF</span><span class="sxs-lookup"><span data-stu-id="cb5d4-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb5d4-412"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cb5d4-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb5d4-413">DLL</span><span class="sxs-lookup"><span data-stu-id="cb5d4-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb5d4-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb5d4-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb5d4-415">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb5d4-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5d4-416">**CIM- \_ processindikation**</span><span class="sxs-lookup"><span data-stu-id="cb5d4-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

