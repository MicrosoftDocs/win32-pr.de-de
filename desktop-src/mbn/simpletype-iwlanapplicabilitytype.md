---
description: Enumeration, die die Art der Netzwerkverbindung beschreibt, in der ein Profil anwendbar ist.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: iwlanApplicabilityType Simple Type
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ede1e4c360bfd88fa8ca0eb3494a9400f4dfc2a1eb70f7857156caabf7b469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035748"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type

Enumeration, die die Art der Netzwerkverbindung beschreibt, in der ein Profil anwendbar ist.

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

Der **einfache Typ iwlanApplicabilityType** definiert die folgenden Werte.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CellularOnly</td>
<td><p>Das Profil ist nur für Mobilfunkverbindungen gültig.</p></td>
</tr>
<tr class="even">
<td>CellularAndIwlan</td>
<td><p>Das Profil ist für mobilfunk- oder Wi-Fi verbindungen gültig.</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>Das Profil ist nur für Wi-Fi verbindungen gültig.</p></td>
</tr>
</tbody>
</table>

 

 



