---
description: Die CIM- \_ Angabe ist die abstrakte Basisklasse für alle Benachrichtigungen über Änderungen in Schema Objekten und Schema Objektdaten, Ereignisse, die von Anbietern und Instrumentation erkannt werden. Unterklassen der CIM- \_ Angabe stellen bestimmte Benachrichtigungs Typen dar.
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373006"
---
# <a name="cim_indication-class"></a><span data-ttu-id="de7fd-104">CIM- \_ Anzeige Klasse</span><span class="sxs-lookup"><span data-stu-id="de7fd-104">CIM\_Indication class</span></span>

<span data-ttu-id="de7fd-105">**CIM \_ Die Angabe** ist die abstrakte Basisklasse für alle Benachrichtigungen über Änderungen in Schema Objekten und Schema Objektdaten, Ereignisse, die von Anbietern und Instrumentation erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="de7fd-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="de7fd-106">Unterklassen der **CIM- \_ Angabe** stellen bestimmte Benachrichtigungs Typen dar.</span><span class="sxs-lookup"><span data-stu-id="de7fd-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="de7fd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de7fd-107">Syntax</span></span>

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a><span data-ttu-id="de7fd-108">Member</span><span class="sxs-lookup"><span data-stu-id="de7fd-108">Members</span></span>

<span data-ttu-id="de7fd-109">Die **CIM- \_ Anzeige** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="de7fd-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="de7fd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de7fd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de7fd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de7fd-111">Properties</span></span>

<span data-ttu-id="de7fd-112">Die **CIM- \_ Anzeige** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de7fd-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de7fd-113">**Correlatedindications**</span><span class="sxs-lookup"><span data-stu-id="de7fd-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-114">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="de7fd-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-116">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Korrelierte Benachrichtigungen "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Angabe**.**Bezeichnerkennung**")</span><span class="sxs-lookup"><span data-stu-id="de7fd-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-117">Ein-Array, das **bezeichnerbezeichnerwerte** von Benachrichtigungen enthält, die mit diesem verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="de7fd-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="de7fd-118">**Bezeichnfiltername**</span><span class="sxs-lookup"><span data-stu-id="de7fd-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de7fd-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-121">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")</span><span class="sxs-lookup"><span data-stu-id="de7fd-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-122">Der Bezeichner des Anzeige Filters, der die Anzeige verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="de7fd-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="de7fd-123">Der sendende Dienst legt diese Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="de7fd-123">The sending service sets this property.</span></span> <span data-ttu-id="de7fd-124">Diese Eigenschaft korreliert mit der **Name** -Eigenschaft des CIM-Objekts " **\_ indicationfilter** ".</span><span class="sxs-lookup"><span data-stu-id="de7fd-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="de7fd-125">Der Wert von " **indicationfiltername** " sollte das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="de7fd-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="de7fd-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="de7fd-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="de7fd-127">*<OrgID>* muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="de7fd-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="de7fd-128">*<OrgID>* darf keinen Doppelpunkt enthalten (:)</span><span class="sxs-lookup"><span data-stu-id="de7fd-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="de7fd-129">*<LocalID>* ein eindeutiger Bezeichner, der von der Geschäfts Entität ausgewählt wird, die das Objekt besitzt</span><span class="sxs-lookup"><span data-stu-id="de7fd-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="de7fd-130">**Bezeichnerkennung**</span><span class="sxs-lookup"><span data-stu-id="de7fd-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de7fd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Benachrichtigungs Bezeichner ")</span><span class="sxs-lookup"><span data-stu-id="de7fd-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-134">Ein Bezeichner des Hinweises.</span><span class="sxs-lookup"><span data-stu-id="de7fd-134">An identifier of the indication.</span></span> <span data-ttu-id="de7fd-135">Diese Eigenschaft kann als Schlüsselwert im **correlatedindications** -Eigenschafts Array verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de7fd-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="de7fd-136">Daher sollte der Wert von " **bezeichationidentifier** " innerhalb des Namespace dieser Klasseninstanz eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="de7fd-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="de7fd-137">Um sicherzustellen, dass " **bezeichationidentifier** " eindeutig ist, sollte das folgende Format verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="de7fd-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="de7fd-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="de7fd-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="de7fd-139">*<OrgID>* muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die das Objekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="de7fd-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="de7fd-140">*<OrgID>* darf keinen Doppelpunkt enthalten (:)</span><span class="sxs-lookup"><span data-stu-id="de7fd-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="de7fd-141">*<LocalID>* ein eindeutiger Bezeichner, der von der Geschäfts Entität ausgewählt wird, die das Objekt besitzt</span><span class="sxs-lookup"><span data-stu-id="de7fd-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="de7fd-142">Für von DMTF definierte Instanzen *<OrgID>* sollte auf "CIM" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="de7fd-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="de7fd-143">**Bezeichationzeit**</span><span class="sxs-lookup"><span data-stu-id="de7fd-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-144">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="de7fd-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-146">Das Datum und die Uhrzeit, zu der die Angabe erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="de7fd-146">The time and date when the indication was created.</span></span> <span data-ttu-id="de7fd-147">Die-Eigenschaft kann auf **null** festgelegt werden, wenn die Entität, die die Angabe erstellt hat, diese Informationen nicht ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="de7fd-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="de7fd-148">Der Wert für " **indicationtime** " kann für in schneller Folge generierte Anzeichen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="de7fd-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="de7fd-149">**Otherschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="de7fd-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de7fd-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-152">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ alertindikation**](cim-alertindication.md)".**Wahrnehmvedschwere Grad**")</span><span class="sxs-lookup"><span data-stu-id="de7fd-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-153">Der Schweregrad der Angabe aus der Sicht des Notifizierers, wenn " **wahrnehmvedschwere Grad** " auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="de7fd-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="de7fd-154">**Wahrnehmgrad**</span><span class="sxs-lookup"><span data-stu-id="de7fd-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de7fd-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-157">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Wahrgenommene Schweregrade ")</span><span class="sxs-lookup"><span data-stu-id="de7fd-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-158">Der Schweregrad der Angabe aus der Sicht des Notifizierers.</span><span class="sxs-lookup"><span data-stu-id="de7fd-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="de7fd-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="de7fd-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-160">der erkannte Schweregrad der Angabe ist unbekannt oder unbestimmt.</span><span class="sxs-lookup"><span data-stu-id="de7fd-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="de7fd-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="de7fd-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-162">Gibt an, dass der Wert des schwere Grads in der Eigenschaft **otherschwere Grad** gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="de7fd-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="de7fd-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="de7fd-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-164">Informationen sollten beim Bereitstellen einer informativen Antwort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de7fd-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="de7fd-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>Heruntergestuft **/Warnung** (3)</span><span class="sxs-lookup"><span data-stu-id="de7fd-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-166">Sollte verwendet werden, wenn der Benutzer die Entscheidung treffen soll, ob eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="de7fd-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="de7fd-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Neben** Version (4)</span><span class="sxs-lookup"><span data-stu-id="de7fd-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-168">Es ist eine Aktion erforderlich, aber die Situation ist zu diesem Zeitpunkt nicht schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="de7fd-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="de7fd-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Haupt** Version (5)</span><span class="sxs-lookup"><span data-stu-id="de7fd-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-170">Die Aktion ist jetzt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de7fd-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="de7fd-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (6)</span><span class="sxs-lookup"><span data-stu-id="de7fd-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-172">Jetzt ist eine Aktion erforderlich, und der Bereich ist umfangreich (möglicherweise kommt es zu einem bevorstehenden Ausfall einer wichtigen Ressource).</span><span class="sxs-lookup"><span data-stu-id="de7fd-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="de7fd-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>Schwerwiegend **/nicht wiederherstellbar** (7)</span><span class="sxs-lookup"><span data-stu-id="de7fd-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="de7fd-174">Es ist ein Fehler aufgetreten, aber es ist zu spät, um Abhilfemaßnahmen zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="de7fd-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="de7fd-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="de7fd-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="de7fd-176">**Sequencecontext**</span><span class="sxs-lookup"><span data-stu-id="de7fd-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de7fd-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-179">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Angabe**.**Sequencenumkehr**")</span><span class="sxs-lookup"><span data-stu-id="de7fd-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-180">Der Sequenz Kontext des Sequenz Bezeichners für die Anzeige.</span><span class="sxs-lookup"><span data-stu-id="de7fd-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="de7fd-181">Wenn ein Dienst keine Sequenz Bezeichner für Hinweise unterstützt, sollte diese Eigenschaft auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="de7fd-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="de7fd-182">Wenn die Angabe erneut übermittelt wird, bleibt diese Eigenschaft unverändert.</span><span class="sxs-lookup"><span data-stu-id="de7fd-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="de7fd-183">Der Sequenz Bezeichner für die Anzeige ermöglicht es einem Listener, doppelte Anzeichen zu identifizieren, wenn der Dienst versucht, Hinweise erneut zu übermitteln, nicht ordnungsgemäß anordnen und damit verlorene Anzeichen erkennen.</span><span class="sxs-lookup"><span data-stu-id="de7fd-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="de7fd-184">Um sicherzustellen, dass **sequencecontext** eindeutig ist, sollte folgendes Format verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="de7fd-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="de7fd-185">*Anzeige Dienst Name* \# *CIM-Service-Start-ID* \# *Listener-Destination-Erstellungszeit*</span><span class="sxs-lookup"><span data-stu-id="de7fd-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="de7fd-186">"Display *-Service-Name* " ist der Wert der " **Name** "-Eigenschaft der CIM-Instanz " **\_ indicationservice** ", die die Anzeige übermittelt.</span><span class="sxs-lookup"><span data-stu-id="de7fd-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="de7fd-187">*CIM-Service-Start-ID ist ein Bezeichner* , der den Startvorgang eines dienstaners eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="de7fd-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="de7fd-188">Dies kann z. b. ein Zeitstempel der Startzeit oder ein Leistungswert sein, der sich für jeden Start-oder Neustart des Dienstanbieter erhöht.</span><span class="sxs-lookup"><span data-stu-id="de7fd-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="de7fd-189">*Listener-Destination-Erstellungszeit* ist ein Zeitstempel der Erstellungszeit der **CIM- \_ listenerdestination** -Instanz, die das Listener-Ziel darstellt. NDA dieses Format nur eine Empfehlung ist, müssen CIM-Clients den Wert als einen nicht transparenten Bezeichner für den Sequenz Kontext behandeln und dürfen sich nicht auf dieses Format verlassen.</span><span class="sxs-lookup"><span data-stu-id="de7fd-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="de7fd-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="de7fd-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de7fd-191">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="de7fd-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de7fd-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de7fd-193">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Angabe**.**Sequencecontext**")</span><span class="sxs-lookup"><span data-stu-id="de7fd-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="de7fd-194">Die Sequenznummer des Sequenz Bezeichners für die Anzeige.</span><span class="sxs-lookup"><span data-stu-id="de7fd-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="de7fd-195">Der Sequenz Bezeichner für die Anzeige ermöglicht es einem Listener, doppelte Anzeichen zu identifizieren, wenn der Dienst versucht, Hinweise erneut zu übermitteln, nicht ordnungsgemäß anordnen und damit verlorene Anzeichen erkennen.</span><span class="sxs-lookup"><span data-stu-id="de7fd-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="de7fd-196">Die Sequenznummer weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="de7fd-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="de7fd-197">Die Sequenznummer wird immer dann auf 0 zurückgesetzt, wenn sich der **sequencecontext** -Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="de7fd-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="de7fd-198">Wenn das listenerziel einen neuen Indikator erhält, wird die Sequenznummer um "1" angehoben.</span><span class="sxs-lookup"><span data-stu-id="de7fd-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="de7fd-199">Die Sequenznummer wird in 0 (null) umschlossen, wenn der Wertebereich überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="de7fd-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="de7fd-200">Wenn die Angabe erneut übermittelt wird, bleibt **SequenceNumber** unverändert.</span><span class="sxs-lookup"><span data-stu-id="de7fd-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de7fd-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de7fd-201">Requirements</span></span>



| <span data-ttu-id="de7fd-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de7fd-202">Requirement</span></span> | <span data-ttu-id="de7fd-203">Wert</span><span class="sxs-lookup"><span data-stu-id="de7fd-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de7fd-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de7fd-204">Minimum supported client</span></span><br/> | <span data-ttu-id="de7fd-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="de7fd-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="de7fd-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de7fd-206">Minimum supported server</span></span><br/> | <span data-ttu-id="de7fd-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="de7fd-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="de7fd-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="de7fd-208">Namespace</span></span><br/>                | <span data-ttu-id="de7fd-209">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="de7fd-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="de7fd-210">MOF</span><span class="sxs-lookup"><span data-stu-id="de7fd-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de7fd-211"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="de7fd-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de7fd-212">DLL</span><span class="sxs-lookup"><span data-stu-id="de7fd-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de7fd-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de7fd-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de7fd-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de7fd-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7fd-215">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="de7fd-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

