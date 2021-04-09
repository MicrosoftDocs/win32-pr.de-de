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
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>einfacher roamapplicabilitytype-Typ

Roamapplicabilitytype beschreibt die roamingbedingungen, für die ein Roamingprofil gilt.

Dabei handelt es sich um ein ausdrucksstarkes Attribut als [**roamcontroltype**](simpletype-roamcontroltype.md), und ein Profil sollte entweder **roamcontroltype** oder **roamapplicabilitytype**, aber nicht beides verwenden. (Wenn ein Profil beides verwendet, werden beide angewendet. Das Ergebnis ist die Schnittmenge der beiden.)

Verwenden Sie dieses Attribut, um zwischen mehreren Profilen mit separaten roamingbedingungen zu unterscheiden, um unterschiedliche Profil Attribute anzugeben, z. b. "Home" und "Roaming".

Es gibt drei mögliche Start-/Roaming-Registrierungs Zustände:

-   Startseite: im Heimnetzwerk registriert
-   Partner: in einem Netzwerk registriert, das eng mit dem Heimnetzwerk verbunden ist
-   Nicht-Partner: in einem Netzwerk registriert, das nicht eng mit dem Heimnetzwerk verbunden ist

Die genaue Bedeutung von "Partner" variiert abhängig vom Netzwerk, stellt jedoch eine engere Beziehung mit günstigeren Tarifen dar als ein nicht Partner. Dies kann der Fall sein, wenn ein Regional basierter Operator über eine geschäftliche Anordnung verfügt, das Funk Zugriffs Netzwerk eines anderen Operators außerhalb seines Startbereichs zu verwenden. Es könnte auch den Unterschied zwischen Roaming innerhalb eines Bereichs (z. b. EU) und außerhalb des Bereichs darstellen.

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

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ **roamapplicabilitytype** definiert die folgenden Werte:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nicht Partnerschaft</td>
<td><p>Dieses Profil wird nur verwendet, wenn das Roaming in einem nicht-Partnernetzwerk erfolgt.</p></td>
</tr>
<tr class="even">
<td>Nur Partner</td>
<td><p>Dieses Profil wird nur beim Roaming in einem Partnernetzwerk verwendet.</p></td>
</tr>
<tr class="odd">
<td>Nur Heim Netz</td>
<td><p>Dieses Profil wird nur im Heimnetzwerk verwendet.</p></td>
</tr>
<tr class="even">
<td>Homeandpartner</td>
<td><p>Dieses Profil wird nur verwendet, wenn es zu Hause oder in einem Partnernetzwerk verwendet wird.</p></td>
</tr>
<tr class="odd">
<td>Partnerandnonpartner</td>
<td><p>Dieses Profil wird verwendet, wenn es nicht zu Hause ist (Roaming in einem beliebigen Netzwerk).</p></td>
</tr>
<tr class="even">
<td>Allroaming</td>
<td><p>Dieses Profil wird in allen Netzwerken verwendet.</p></td>
</tr>
</tbody>
</table>

 

 



