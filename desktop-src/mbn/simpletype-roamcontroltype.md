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
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamcontroltype simple-Typ

Beschreibt die Steuerung des Roamings durch das Profil.

Es gibt zwei mögliche Roaming-Registrierungs Zustände:

-   Partner: in einem Netzwerk registriert, das eng mit dem Heimnetzwerk verbunden ist
-   Nicht-Partner: in einem Netzwerk registriert, das nicht eng mit dem Heimnetzwerk verbunden ist

Die genaue Bedeutung von "Partner" variiert abhängig vom Netzwerk, stellt jedoch eine engere Beziehung mit günstigeren Tarifen dar als ein nicht Partner. Dies kann der Fall sein, wenn ein Regional basierter Operator über eine geschäftliche Anordnung verfügt, das Funk Zugriffs Netzwerk eines anderen Operators außerhalb seines Startbereichs zu verwenden. Es könnte auch den Unterschied zwischen Roaming innerhalb eines Bereichs (z. b. EU) und außerhalb des Bereichs darstellen.

Beachten Sie, dass [**roamapplicabilitytype**](simpletype-roamapplicabilitytype.md) ein ausdrucksstarkes Attribut ist als **roamcontroltype**, und ein Profil muss entweder **roamcontroltype** oder **roamapplicabilitytype**, aber nicht beides verwenden. (Wenn ein Profil beides verwendet, werden beide angewendet. Das Ergebnis ist die Schnittmenge der beiden.)

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

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache **roamcontroltype** -Typ definiert die folgenden Werte.

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
<td>Allroamallowed</td>
<td><p>Roaming ist für Partnernetzwerke und nicht Partnernetzwerke zulässig.</p></td>
</tr>
<tr class="even">
<td>Partnerroamamallowed</td>
<td><p>Roaming ist nur in Partner Netzwerken zulässig.</p></td>
</tr>
<tr class="odd">
<td>Noroamallowed</td>
<td><p>Es ist kein Roaming zulässig.</p></td>
</tr>
</tbody>
</table>

 

 



