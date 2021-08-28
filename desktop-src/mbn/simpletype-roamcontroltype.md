---
description: Beschreibt, wie das Profil das Roaming steuert.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamControlType Simple Type
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19243625c07afae49011638a37734a5515e626d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480236"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType – einfacher Typ

Beschreibt, wie das Profil das Roaming steuert.

Es gibt zwei mögliche Roamingregistrierungszustände:

-   Partner: Registriert in einem Netzwerk, das eng mit dem Heimnetzwerk verbunden ist
-   Nicht-Partner: Registriert in einem Netzwerk, das nicht eng mit dem Heimnetzwerk verbunden ist

Die genaue Bedeutung von "Partner" variiert je nach Netzwerk, stellt aber eine genauere Beziehung mit günstigeren Preisen als ein Nicht-Partner dar. Dies kann der Fall sein, wenn ein regionsbasierter Operator über eine Geschäftsanordnung verfügt, um das Funkzugriffsnetzwerk eines anderen Betreibers außerhalb seines Stammbereichs zu verwenden. Sie kann auch den Unterschied zwischen roaming innerhalb einer Region (z. B. EU) und außerhalb davon darstellen.

Beachten Sie, dass [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) ein ausdrucksstärkeres Attribut als **roamControlType** ist, und ein Profil sollte entweder **roamControlType** oder **roamApplicabilityType** verwenden, aber nicht beides. (Wenn ein Profil beide verwendet, werden beide angewendet. Das Ergebnis ist die Schnittmenge der beiden.)

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

Der einfache typ **roamControlType** definiert die folgenden Werte.


| Wert | BESCHREIBUNG | 
|-------|-------------|
| AllRoamAllowed | <p>Roaming ist in Partner- und Nicht-Partnernetzwerken zulässig.</p> | 
| PartnerRoamAllowed | <p>Roaming ist nur in Partnernetzwerken zulässig.</p> | 
| NoRoamAllowed | <p>Roaming ist nicht zulässig.</p> | 


 

 



