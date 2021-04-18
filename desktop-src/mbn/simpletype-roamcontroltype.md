---
description: Beschreibt die Steuerung des Roamings durch das Profil.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamcontroltype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343697"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="b05b9-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamcontroltype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="b05b9-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="b05b9-104">Beschreibt die Steuerung des Roamings durch das Profil.</span><span class="sxs-lookup"><span data-stu-id="b05b9-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="b05b9-105">Es gibt zwei mögliche Roaming-Registrierungs Zustände:</span><span class="sxs-lookup"><span data-stu-id="b05b9-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="b05b9-106">Partner: in einem Netzwerk registriert, das eng mit dem Heimnetzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="b05b9-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="b05b9-107">Nicht-Partner: in einem Netzwerk registriert, das nicht eng mit dem Heimnetzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="b05b9-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="b05b9-108">Die genaue Bedeutung von "Partner" variiert abhängig vom Netzwerk, stellt jedoch eine engere Beziehung mit günstigeren Tarifen dar als ein nicht Partner.</span><span class="sxs-lookup"><span data-stu-id="b05b9-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="b05b9-109">Dies kann der Fall sein, wenn ein Regional basierter Operator über eine geschäftliche Anordnung verfügt, das Funk Zugriffs Netzwerk eines anderen Operators außerhalb seines Startbereichs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b05b9-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="b05b9-110">Es könnte auch den Unterschied zwischen Roaming innerhalb eines Bereichs (z. b. EU) und außerhalb des Bereichs darstellen.</span><span class="sxs-lookup"><span data-stu-id="b05b9-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="b05b9-111">Beachten Sie, dass [**roamapplicabilitytype**](simpletype-roamapplicabilitytype.md) ein ausdrucksstarkes Attribut ist als **roamcontroltype**, und ein Profil muss entweder **roamcontroltype** oder **roamapplicabilitytype**, aber nicht beides verwenden.</span><span class="sxs-lookup"><span data-stu-id="b05b9-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="b05b9-112">(Wenn ein Profil beides verwendet, werden beide angewendet.</span><span class="sxs-lookup"><span data-stu-id="b05b9-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="b05b9-113">Das Ergebnis ist die Schnittmenge der beiden.)</span><span class="sxs-lookup"><span data-stu-id="b05b9-113">The result is the intersection of the two.)</span></span>

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="b05b9-114">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="b05b9-114">Enumeration values</span></span>

<span data-ttu-id="b05b9-115">Der einfache **roamcontroltype** -Typ definiert die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="b05b9-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b05b9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b05b9-116">Value</span></span></th>
<th><span data-ttu-id="b05b9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b05b9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b05b9-118">Allroamallowed</span><span class="sxs-lookup"><span data-stu-id="b05b9-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="b05b9-119">Roaming ist für Partnernetzwerke und nicht Partnernetzwerke zulässig.</span><span class="sxs-lookup"><span data-stu-id="b05b9-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b05b9-120">Partnerroamamallowed</span><span class="sxs-lookup"><span data-stu-id="b05b9-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="b05b9-121">Roaming ist nur in Partner Netzwerken zulässig.</span><span class="sxs-lookup"><span data-stu-id="b05b9-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b05b9-122">Noroamallowed</span><span class="sxs-lookup"><span data-stu-id="b05b9-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="b05b9-123">Es ist kein Roaming zulässig.</span><span class="sxs-lookup"><span data-stu-id="b05b9-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



