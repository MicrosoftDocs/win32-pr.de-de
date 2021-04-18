---
description: Beschreibt die Einschränkungen für die Eigenschaften eines zugeordneten CIM \_ enabledlogicalelement-Objekts.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359083"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="75744-103">CIM \_ enabledlogicalelementfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="75744-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="75744-104">Beschreibt die Einschränkungen für die Eigenschaften eines zugeordneten [**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="75744-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75744-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75744-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="75744-106">Member</span><span class="sxs-lookup"><span data-stu-id="75744-106">Members</span></span>

<span data-ttu-id="75744-107">Die **CIM \_ enabledlogicalelementfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="75744-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="75744-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75744-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75744-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75744-109">Properties</span></span>

<span data-ttu-id="75744-110">Die **CIM \_ enabledlogicalelementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="75744-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75744-111">**Elementnameeditsupported**</span><span class="sxs-lookup"><span data-stu-id="75744-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75744-112">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="75744-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="75744-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="75744-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75744-114">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-Swap. "INCITS-T11 \| \_ \_ \_ \_ \| ", "", "", "", [](/windows/desktop/WmiSdk/standard-qualifiers) "", "", "", "", "[**CIM \_ managedelta**](cim-managedelement.md)".**Elementname**")</span><span class="sxs-lookup"><span data-stu-id="75744-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="75744-115">**true** , wenn die **ElementName** -Eigenschaft des aktivierten logischen Elements geändert werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="75744-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="75744-116">**Elementnamemask**</span><span class="sxs-lookup"><span data-stu-id="75744-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75744-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="75744-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75744-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="75744-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75744-119">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelementutilities**".**Maxelementnamelen**")</span><span class="sxs-lookup"><span data-stu-id="75744-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="75744-120">Ein regulärer Ausdruck, der die Einschränkungen für die Element **Name** -Eigenschaft des logischen Elements enable angibt.</span><span class="sxs-lookup"><span data-stu-id="75744-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="75744-121">Die zulässige Syntax finden Sie unter *DMTF Standard ABNF mit dem Verwendungs Handbuch zur Verwaltungs Profil Spezifikation*(Anhang C).</span><span class="sxs-lookup"><span data-stu-id="75744-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="75744-122">Wenn diese Eigenschaft und die **elementnamemask** -Eigenschaft des logischen Elements enable die maximale Länge von Element **Name** beschreiben, wird der kleinere Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="75744-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="75744-123">**Maxelementnamelen**</span><span class="sxs-lookup"><span data-stu-id="75744-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75744-124">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="75744-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="75744-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="75744-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75744-126">Qualifizierer: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-Swap-API. INCITS-T11-- \| \_ Einheiten config-Einheiten \_ config \_ \_ T \| maxnamechars "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ fcswitchfunktionalitäten. elementnameeditsupported ","**CIM \_ enabledlogicalelementutilities**".**Elementnamemask**")</span><span class="sxs-lookup"><span data-stu-id="75744-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="75744-127">Die maximal unterstützte Länge der **ElementName** -Eigenschaft des aktivierten logischen Elements.</span><span class="sxs-lookup"><span data-stu-id="75744-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="75744-128">**Requestedstaatunter stützt**</span><span class="sxs-lookup"><span data-stu-id="75744-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75744-129">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="75744-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="75744-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="75744-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75744-131">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**RequestStateChange**")</span><span class="sxs-lookup"><span data-stu-id="75744-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="75744-132">Die möglichen Zustände, die von der [**requestStateChange**](cim-enabledlogicalelement-requeststatechange.md) -Methode auf dem aktivierten logischen Element angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="75744-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="75744-133">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="75744-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="75744-134">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="75744-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="75744-135">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="75744-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="75744-136">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="75744-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="75744-137">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="75744-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="75744-138">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="75744-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="75744-139">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="75744-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="75744-140">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="75744-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="75744-141">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="75744-141">**Reset** (11)</span></span>


<span data-ttu-id="75744-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="75744-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="75744-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75744-143">Requirements</span></span>



| <span data-ttu-id="75744-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75744-144">Requirement</span></span> | <span data-ttu-id="75744-145">Wert</span><span class="sxs-lookup"><span data-stu-id="75744-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75744-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75744-146">Minimum supported client</span></span><br/> | <span data-ttu-id="75744-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="75744-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="75744-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75744-148">Minimum supported server</span></span><br/> | <span data-ttu-id="75744-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75744-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="75744-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="75744-150">Namespace</span></span><br/>                | <span data-ttu-id="75744-151">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="75744-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="75744-152">MOF</span><span class="sxs-lookup"><span data-stu-id="75744-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75744-153"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="75744-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75744-154">DLL</span><span class="sxs-lookup"><span data-stu-id="75744-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75744-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75744-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75744-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75744-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75744-157">**CIM- \_ Funktionen**</span><span class="sxs-lookup"><span data-stu-id="75744-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

