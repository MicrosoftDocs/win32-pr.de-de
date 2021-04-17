---
description: Enumeration, die die Art der Netzwerkverbindung beschreibt, auf die ein Profil anwendbar ist.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: einfacher iwlanapplicabilitytype-Typ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526615"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>einfacher iwlanapplicabilitytype-Typ

Enumeration, die die Art der Netzwerkverbindung beschreibt, auf die ein Profil anwendbar ist.

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ " **iwlanapplicabilitytype** " definiert die folgenden Werte:

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
<td>Cellularonly</td>
<td><p>Das Profil ist nur für Mobilfunknetzwerk Verbindungen gültig.</p></td>
</tr>
<tr class="even">
<td>Cellularandiwlan</td>
<td><p>Das Profil ist für Mobilfunk-oder Wi-Fi offloaded-Verbindungen gültig.</p></td>
</tr>
<tr class="odd">
<td>Iwlanonly</td>
<td><p>Das Profil ist nur für Wi-Fi offloaded-Verbindungen gültig.</p></td>
</tr>
</tbody>
</table>

 

 



