---
description: Beschreibt eine Reihe von Klassen mit erforderlichen Eigenschaften und Methoden, die zum Verwalten einer realen Entität oder zur Unterstützung eines Verwendungs Szenarios auf interoperable Weise erforderlich sind.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Msvm_RegisteredProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042327"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="7ac78-103">MSVM \_ registeredprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="7ac78-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="7ac78-104">Beschreibt eine Reihe von Klassen mit erforderlichen Eigenschaften und Methoden, die zum Verwalten einer realen Entität oder zur Unterstützung eines Verwendungs Szenarios auf interoperable Weise erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7ac78-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="7ac78-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ac78-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac78-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ac78-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="7ac78-107">Member</span><span class="sxs-lookup"><span data-stu-id="7ac78-107">Members</span></span>

<span data-ttu-id="7ac78-108">Die **MSVM \_ registeredprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7ac78-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="7ac78-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ac78-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ac78-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ac78-110">Properties</span></span>

<span data-ttu-id="7ac78-111">Die **MSVM \_ registeredprofile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ac78-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ac78-112">**"Werbe Beschreibungen"**</span><span class="sxs-lookup"><span data-stu-id="7ac78-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7ac78-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-115">Ein Array von Zeichen folgen, das zusätzliche Informationen bereitstellt, die sich auf die " **Werbung** "-Eigenschaft beziehen.</span><span class="sxs-lookup"><span data-stu-id="7ac78-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="7ac78-116">Es muss eine Beschreibung angegeben werden, wenn der **Typ** von "1 (sonstige)" lautet.</span><span class="sxs-lookup"><span data-stu-id="7ac78-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="7ac78-117">Ein Eintrag in diesem Array entspricht dem gleichen Index im **Werbe Types** -Array.</span><span class="sxs-lookup"><span data-stu-id="7ac78-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="7ac78-118">Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-119">**Werbung Typen**</span><span class="sxs-lookup"><span data-stu-id="7ac78-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-120">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7ac78-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-122">Gibt die Ankündigung für die Profilinformationen an.</span><span class="sxs-lookup"><span data-stu-id="7ac78-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="7ac78-123">Sie wird von den Ankündigungs Diensten der WBEM-Infrastruktur verwendet, um zu bestimmen, was durch welche Mechanismen angekündigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ac78-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="7ac78-124">Die-Eigenschaft ist ein Array, sodass das Profil mithilfe verschiedener Mechanismen angekündigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ac78-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="7ac78-125">Wenn diese Eigenschaft **null** ist, entspricht dies der Angabe des Werts 2 (nicht angekündigt).</span><span class="sxs-lookup"><span data-stu-id="7ac78-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="7ac78-126">Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7ac78-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7ac78-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Nicht angekündigt** (2)</span><span class="sxs-lookup"><span data-stu-id="7ac78-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3)</span><span class="sxs-lookup"><span data-stu-id="7ac78-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ac78-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7ac78-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-133">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ac78-133">A short description of the object.</span></span> <span data-ttu-id="7ac78-134">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ac78-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-138">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ac78-138">A description of the object.</span></span> <span data-ttu-id="7ac78-139">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7ac78-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-143">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-143">A display name for the object.</span></span> <span data-ttu-id="7ac78-144">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ac78-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-148">Qualifizierer: **Key**, **override**</span><span class="sxs-lookup"><span data-stu-id="7ac78-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-149">Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7ac78-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7ac78-150">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-151">**Otherregisteredorganization**</span><span class="sxs-lookup"><span data-stu-id="7ac78-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-154">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7ac78-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-155">Eine Zeichenfolge, die eine Beschreibung der Organisation bereitstellt, wenn **RegisteredOrganization** 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="7ac78-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="7ac78-156">Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-157">**Registeredname**</span><span class="sxs-lookup"><span data-stu-id="7ac78-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-160">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7ac78-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-161">Der Name dieses registrierten Profils.</span><span class="sxs-lookup"><span data-stu-id="7ac78-161">The name of this registered profile.</span></span> <span data-ttu-id="7ac78-162">Da für denselben **registeredname** mehrere Versionen vorhanden sein können, muss die Kombination von **registeredname**, **RegisteredOrganization** und **registeredversion** das registrierte Profil innerhalb des Bereichs der Organisation eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7ac78-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="7ac78-163">Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ac78-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="7ac78-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ac78-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-167">Die Organisation, die dieses Profil definiert.</span><span class="sxs-lookup"><span data-stu-id="7ac78-167">The organization that defines this profile.</span></span> <span data-ttu-id="7ac78-168">Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7ac78-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7ac78-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span><span class="sxs-lookup"><span data-stu-id="7ac78-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span><span class="sxs-lookup"><span data-stu-id="7ac78-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Konsortium für Dienst Innovation** (4)</span><span class="sxs-lookup"><span data-stu-id="7ac78-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-173"><span id="FAST"></span><span id="fast"></span>**Schnell** (5)</span><span class="sxs-lookup"><span data-stu-id="7ac78-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-174"><span id="GGF"></span><span id="ggf"></span>**Ggf** . (6)</span><span class="sxs-lookup"><span data-stu-id="7ac78-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-175"><span id="INTAP"></span><span id="intap"></span>**Einzug** (7)</span><span class="sxs-lookup"><span data-stu-id="7ac78-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span><span class="sxs-lookup"><span data-stu-id="7ac78-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span><span class="sxs-lookup"><span data-stu-id="7ac78-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10 Nordwest-Energieeffizienz-Alliance** (10)</span><span class="sxs-lookup"><span data-stu-id="7ac78-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-179"><span id="SNIA"></span><span id="snia"></span>**Sja** (11)</span><span class="sxs-lookup"><span data-stu-id="7ac78-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM-Forum** (12)</span><span class="sxs-lookup"><span data-stu-id="7ac78-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Die geöffnete Gruppe** (13)</span><span class="sxs-lookup"><span data-stu-id="7ac78-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span><span class="sxs-lookup"><span data-stu-id="7ac78-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span><span class="sxs-lookup"><span data-stu-id="7ac78-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span><span class="sxs-lookup"><span data-stu-id="7ac78-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span><span class="sxs-lookup"><span data-stu-id="7ac78-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span><span class="sxs-lookup"><span data-stu-id="7ac78-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span><span class="sxs-lookup"><span data-stu-id="7ac78-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 OGF** . (20)</span><span class="sxs-lookup"><span data-stu-id="7ac78-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Grünes Raster** (21)</span><span class="sxs-lookup"><span data-stu-id="7ac78-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="7ac78-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7ac78-191">)</span><span class="sxs-lookup"><span data-stu-id="7ac78-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ac78-192">**Registeredversion**</span><span class="sxs-lookup"><span data-stu-id="7ac78-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ac78-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ac78-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ac78-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ac78-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ac78-195">Die Version dieses Profils.</span><span class="sxs-lookup"><span data-stu-id="7ac78-195">The version of this profile.</span></span> <span data-ttu-id="7ac78-196">Die Zeichenfolge muss folgendes Format aufweisen: "*M*. *N*. *U*"WHERE:</span><span class="sxs-lookup"><span data-stu-id="7ac78-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="7ac78-197">*M* ist die Hauptversion (in numerischer Form), in der die Profilerstellung oder die letzte Änderung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7ac78-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="7ac78-198">*N* ist die neben Version (in numerischer Form), in der die Profilerstellung oder die letzte Änderung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7ac78-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="7ac78-199">*U* ist das Update (in numerischer Form), das die Profilerstellung oder die letzte Änderung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="7ac78-200">Diese Eigenschaft wird von [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ac78-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ac78-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ac78-201">Requirements</span></span>



| <span data-ttu-id="7ac78-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ac78-202">Requirement</span></span> | <span data-ttu-id="7ac78-203">Wert</span><span class="sxs-lookup"><span data-stu-id="7ac78-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac78-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ac78-204">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac78-205">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7ac78-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7ac78-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ac78-206">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac78-207">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ac78-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7ac78-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ac78-208">Namespace</span></span><br/>                | <span data-ttu-id="7ac78-209">Root- \\ Interop</span><span class="sxs-lookup"><span data-stu-id="7ac78-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="7ac78-210">MOF</span><span class="sxs-lookup"><span data-stu-id="7ac78-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ac78-211"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ac78-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ac78-212">DLL</span><span class="sxs-lookup"><span data-stu-id="7ac78-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ac78-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ac78-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

