---
description: Stellt ein logisches Element dar, das aktiviert und deaktiviert werden kann.
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: CIM_EnabledLogicalElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359084"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="e1760-103">CIM \_ enabledlogicalelement-Klasse</span><span class="sxs-lookup"><span data-stu-id="e1760-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="e1760-104">Stellt ein logisches Element dar, das aktiviert und deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1760-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1760-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1760-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="e1760-106">Member</span><span class="sxs-lookup"><span data-stu-id="e1760-106">Members</span></span>

<span data-ttu-id="e1760-107">Die **CIM \_ enabledlogicalelement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e1760-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e1760-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1760-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="e1760-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1760-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e1760-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1760-110">Methods</span></span>

<span data-ttu-id="e1760-111">Die **CIM \_ enabledlogicalelement** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e1760-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="e1760-112">Methode</span><span class="sxs-lookup"><span data-stu-id="e1760-112">Method</span></span>                                                                     | <span data-ttu-id="e1760-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1760-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1760-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e1760-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="e1760-115">Fordert an, dass der Zustand des Elements in den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e1760-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e1760-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1760-116">Properties</span></span>

<span data-ttu-id="e1760-117">Die **CIM \_ enabledlogicalelement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e1760-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1760-118">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="e1760-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-119">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e1760-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1760-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1760-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1760-121">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelement**".**RequestStateChange**","[**CIM \_ enabledlogicalelementfunktionen**](cim-enabledlogicalelementcapabilities.md).**Requestedstaatunter stützt**")</span><span class="sxs-lookup"><span data-stu-id="e1760-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="e1760-122">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](cim-enabledlogicalelement-requeststatechange.md) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="e1760-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="e1760-123">Die aufgelisteten Werte müssen eine Teilmenge der Werte sein, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten **CIM \_ enabledlogicalelementfunktionalitäten** -Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e1760-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="e1760-124">Diese Eigenschaft ist **null** , wenn die Implementierung den Satz möglicher Werte für den aktuellen Zustand des Elements nicht ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="e1760-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e1760-125">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e1760-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e1760-126">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e1760-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="e1760-127">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="e1760-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="e1760-128">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e1760-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e1760-129">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e1760-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="e1760-130">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="e1760-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e1760-131">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="e1760-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="e1760-132">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="e1760-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e1760-133">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="e1760-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1760-134">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1760-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1760-135">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="e1760-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-136">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1760-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1760-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e1760-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e1760-138">Gibt die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="e1760-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e1760-139">Der **aktivierte** Standardwert (2).</span><span class="sxs-lookup"><span data-stu-id="e1760-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e1760-140">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e1760-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e1760-141">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e1760-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1760-142">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="e1760-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="e1760-143">**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e1760-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="e1760-144">**Kein Standard** Wert (7)</span><span class="sxs-lookup"><span data-stu-id="e1760-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e1760-145">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="e1760-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1760-146">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1760-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1760-147">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e1760-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1760-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e1760-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1760-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1760-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1760-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1760-151">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelement**".**Otherenabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e1760-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e1760-152">Gibt den aktivierten Zustand eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="e1760-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="e1760-153">Mögliche Werte sind die Übergänge zwischen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="e1760-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="e1760-154">Das **Herunterfahren (4** ) und das **starten** (10) sind z. b. vorübergehende Zustände zwischen **aktiviertem** und **deaktiviertem** Zustand.</span><span class="sxs-lookup"><span data-stu-id="e1760-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1760-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e1760-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e1760-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="e1760-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e1760-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e1760-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-158">Das-Element ist oder kann Befehle ausführen, verarbeitet alle in der Warteschlange befindlichen Befehle und fügt neue Anforderungen in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="e1760-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e1760-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e1760-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-160">das-Element führt keine Befehle aus und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="e1760-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="e1760-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="e1760-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-162">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="e1760-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1760-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="e1760-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-164">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="e1760-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="e1760-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e1760-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-166">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="e1760-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e1760-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e1760-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-168">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="e1760-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="e1760-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="e1760-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-170">Das Element kann Befehle abschließen, aber alle neuen Anforderungen in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="e1760-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e1760-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="e1760-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-172">, Wenn das Element aktiviert ist, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="e1760-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e1760-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (10)</span><span class="sxs-lookup"><span data-stu-id="e1760-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-174">Das Element wechselt in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="e1760-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="e1760-175">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="e1760-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1760-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (11.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e1760-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1760-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e1760-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1760-178">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="e1760-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1760-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1760-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1760-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1760-181">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelement**".**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e1760-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e1760-182">Beschreibt den Zustand des Elements, wenn der Wert der **enabledstate** -Eigenschaft ein **anderer** Wert ist.</span><span class="sxs-lookup"><span data-stu-id="e1760-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="e1760-183">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** nicht **anders** ist.</span><span class="sxs-lookup"><span data-stu-id="e1760-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="e1760-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e1760-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1760-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1760-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1760-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1760-187">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelement**".**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e1760-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e1760-188">Gibt den letzten angeforderten Zustand für das Element an.</span><span class="sxs-lookup"><span data-stu-id="e1760-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="e1760-189">Der aktuelle Zustand wird durch die **enabledstate** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="e1760-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="e1760-190">Mit dieser Eigenschaft können Sie die zuletzt angeforderten und aktuellen Zustände vergleichen.</span><span class="sxs-lookup"><span data-stu-id="e1760-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="e1760-191">Wenn der Wert der **enabledstate** -Eigenschaft **nicht anwendbar** ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="e1760-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1760-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e1760-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-193">Der zuletzt angeforderte Status für das Element ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e1760-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e1760-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e1760-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e1760-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e1760-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-196">Fordert eine sofortige Deaktivierung des-Elements an, sodass keine Befehle oder Verarbeitungsanforderungen ausgeführt oder akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="e1760-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="e1760-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="e1760-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-198">Fordert einen ordnungsgemäßen Übergang in den deaktivierten Zustand an und kann dazu führen, dass die Stromversorgung vollständig gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e1760-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="e1760-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Keine Änderung** (5)</span><span class="sxs-lookup"><span data-stu-id="e1760-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-200">Wurde als veraltet markiert, um anzugeben, dass der zuletzt angeforderte Status "unknown" (0) ist.</span><span class="sxs-lookup"><span data-stu-id="e1760-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="e1760-201">Wenn der zuletzt angeforderte oder gewünschte Zustand unbekannt ist, sollte **requestedstate** den Wert "unknown" (0) aufweisen, aber möglicherweise den Wert "keine Änderung" (5).</span><span class="sxs-lookup"><span data-stu-id="e1760-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="e1760-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e1760-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-203">Das Element wurde aufgefordert, in den aktivierten, aber offline- **enabledstate** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="e1760-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e1760-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e1760-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="e1760-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="e1760-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e1760-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="e1760-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="e1760-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="e1760-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-208">Bezieht sich auf das Herunterfahren und anschließende verschieben in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="e1760-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e1760-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="e1760-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="e1760-210">Gibt an, dass das Element zuerst "deaktiviert" und dann "aktiviert" ist.</span><span class="sxs-lookup"><span data-stu-id="e1760-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1760-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (12)</span><span class="sxs-lookup"><span data-stu-id="e1760-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1760-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1760-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1760-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e1760-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1760-214">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="e1760-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-215">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1760-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1760-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1760-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1760-217">Gibt an, wann der Zustand des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e1760-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="e1760-218">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e1760-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="e1760-219">Wenn eine Zustandsänderung angefordert wurde, aber abgelehnt wurde oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e1760-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="e1760-220">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="e1760-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1760-221">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1760-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1760-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1760-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1760-223">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ enabledlogicalelement**".**RequestStateChange**","**CIM \_ enabledlogicalelement**.**Requestedstate**","**CIM \_ enabledlogicalelement**.**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="e1760-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="e1760-224">Gibt den Ziel Status an, in dem die-Instanz geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e1760-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="e1760-225">Der Wert **keine Änderung** bedeutet, dass kein Übergang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1760-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="e1760-226">Der Wert **nicht zutreffend** gibt an, dass die Implementierung keine laufenden Übergänge meldet.</span><span class="sxs-lookup"><span data-stu-id="e1760-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1760-227">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e1760-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e1760-228">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e1760-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e1760-229">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e1760-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="e1760-230">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="e1760-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="e1760-231">**Keine Änderung** (5)</span><span class="sxs-lookup"><span data-stu-id="e1760-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="e1760-232">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e1760-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e1760-233">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e1760-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="e1760-234">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="e1760-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="e1760-235">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="e1760-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="e1760-236">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="e1760-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="e1760-237">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="e1760-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1760-238">**Nicht zutreffend** (12)</span><span class="sxs-lookup"><span data-stu-id="e1760-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1760-239">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1760-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="e1760-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e1760-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e1760-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1760-241">Requirements</span></span>



| <span data-ttu-id="e1760-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1760-242">Requirement</span></span> | <span data-ttu-id="e1760-243">Wert</span><span class="sxs-lookup"><span data-stu-id="e1760-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1760-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1760-244">Minimum supported client</span></span><br/> | <span data-ttu-id="e1760-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e1760-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e1760-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1760-246">Minimum supported server</span></span><br/> | <span data-ttu-id="e1760-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1760-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e1760-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1760-248">Namespace</span></span><br/>                | <span data-ttu-id="e1760-249">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e1760-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e1760-250">MOF</span><span class="sxs-lookup"><span data-stu-id="e1760-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1760-251"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e1760-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1760-252">DLL</span><span class="sxs-lookup"><span data-stu-id="e1760-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1760-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1760-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1760-254">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1760-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1760-255">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e1760-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

