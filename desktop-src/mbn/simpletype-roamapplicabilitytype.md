---
description: Roamapplicabilitytype beschreibt die roamingbedingungen, für die ein Roamingprofil gilt.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: einfacher roamapplicabilitytype-Typ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862504"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="b3d87-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>einfacher roamapplicabilitytype-Typ</span><span class="sxs-lookup"><span data-stu-id="b3d87-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="b3d87-104">Roamapplicabilitytype beschreibt die roamingbedingungen, für die ein Roamingprofil gilt.</span><span class="sxs-lookup"><span data-stu-id="b3d87-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="b3d87-105">Dabei handelt es sich um ein ausdrucksstarkes Attribut als [**roamcontroltype**](simpletype-roamcontroltype.md), und ein Profil sollte entweder **roamcontroltype** oder **roamapplicabilitytype**, aber nicht beides verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3d87-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="b3d87-106">(Wenn ein Profil beides verwendet, werden beide angewendet.</span><span class="sxs-lookup"><span data-stu-id="b3d87-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="b3d87-107">Das Ergebnis ist die Schnittmenge der beiden.)</span><span class="sxs-lookup"><span data-stu-id="b3d87-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="b3d87-108">Verwenden Sie dieses Attribut, um zwischen mehreren Profilen mit separaten roamingbedingungen zu unterscheiden, um unterschiedliche Profil Attribute anzugeben, z. b. "Home" und "Roaming".</span><span class="sxs-lookup"><span data-stu-id="b3d87-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="b3d87-109">Es gibt drei mögliche Start-/Roaming-Registrierungs Zustände:</span><span class="sxs-lookup"><span data-stu-id="b3d87-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="b3d87-110">Startseite: im Heimnetzwerk registriert</span><span class="sxs-lookup"><span data-stu-id="b3d87-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="b3d87-111">Partner: in einem Netzwerk registriert, das eng mit dem Heimnetzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="b3d87-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="b3d87-112">Nicht-Partner: in einem Netzwerk registriert, das nicht eng mit dem Heimnetzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="b3d87-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="b3d87-113">Die genaue Bedeutung von "Partner" variiert abhängig vom Netzwerk, stellt jedoch eine engere Beziehung mit günstigeren Tarifen dar als ein nicht Partner.</span><span class="sxs-lookup"><span data-stu-id="b3d87-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="b3d87-114">Dies kann der Fall sein, wenn ein Regional basierter Operator über eine geschäftliche Anordnung verfügt, das Funk Zugriffs Netzwerk eines anderen Operators außerhalb seines Startbereichs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3d87-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="b3d87-115">Es könnte auch den Unterschied zwischen Roaming innerhalb eines Bereichs (z. b. EU) und außerhalb des Bereichs darstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d87-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="b3d87-116">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="b3d87-116">Enumeration values</span></span>

<span data-ttu-id="b3d87-117">Der einfache Typ **roamapplicabilitytype** definiert die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="b3d87-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3d87-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b3d87-118">Value</span></span></th>
<th><span data-ttu-id="b3d87-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3d87-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3d87-120">Nicht Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3d87-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="b3d87-121">Dieses Profil wird nur verwendet, wenn das Roaming in einem nicht-Partnernetzwerk erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b3d87-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d87-122">Nur Partner</span><span class="sxs-lookup"><span data-stu-id="b3d87-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="b3d87-123">Dieses Profil wird nur beim Roaming in einem Partnernetzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3d87-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3d87-124">Nur Heim Netz</span><span class="sxs-lookup"><span data-stu-id="b3d87-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="b3d87-125">Dieses Profil wird nur im Heimnetzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3d87-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d87-126">Homeandpartner</span><span class="sxs-lookup"><span data-stu-id="b3d87-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="b3d87-127">Dieses Profil wird nur verwendet, wenn es zu Hause oder in einem Partnernetzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3d87-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3d87-128">Partnerandnonpartner</span><span class="sxs-lookup"><span data-stu-id="b3d87-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="b3d87-129">Dieses Profil wird verwendet, wenn es nicht zu Hause ist (Roaming in einem beliebigen Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="b3d87-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d87-130">Allroaming</span><span class="sxs-lookup"><span data-stu-id="b3d87-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="b3d87-131">Dieses Profil wird in allen Netzwerken verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3d87-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



