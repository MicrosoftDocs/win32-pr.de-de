---
description: Enumeration, die die Art der Netzwerkverbindung beschreibt, für die ein Profil anwendbar ist.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Einfacher iwlanApplicabilityType-Typ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529ae39c2b0e137825e7a80d41c43203b0a27de7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478956"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Einfacher iwlanApplicabilityType-Typ

Enumeration, die die Art der Netzwerkverbindung beschreibt, für die ein Profil anwendbar ist.

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

Der einfache Typ **iwlanApplicabilityType** definiert die folgenden Werte.


| Wert | BESCHREIBUNG | 
|-------|-------------|
| CellularOnly | <p>Das Profil ist nur für Mobilfunknetzverbindungen gültig.</p> | 
| CellularAndIwlan | <p>Das Profil ist für mobilfunk- oder Wi-Fi ausgelagerte Verbindungen gültig.</p> | 
| IwlanOnly | <p>Das Profil ist nur für Wi-Fi ausgelagerte Verbindungen gültig.</p> | 


 

 



