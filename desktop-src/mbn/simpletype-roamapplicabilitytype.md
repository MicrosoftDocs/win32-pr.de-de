---
description: RoamApplicabilityType beschreibt die Roamingbedingungen, für die ein Roamingprofil gilt.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamApplicabilityType Simple Type
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2ce8f24e0987d5e8463838b33d4f2f2cf859da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474756"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type

RoamApplicabilityType beschreibt die Roamingbedingungen, für die ein Roamingprofil gilt.

Dies ist ein ausdrucksstärkeres Attribut als [**roamControlType,**](simpletype-roamcontroltype.md)und ein Profil sollte entweder **roamControlType** oder **roamApplicabilityType** verwenden, aber nicht beides. (Wenn ein Profil beides verwendet, werden beide angewendet. Das Ergebnis ist die Schnittmenge der beiden.)

Verwenden Sie dieses Attribut, um zwischen mehreren Profilen mit unterschiedlichen Roamingbedingungen zu unterscheiden, um unterschiedliche Profilattribute für z. B. "Home" und "Roaming" anzugeben.

Es gibt drei mögliche Registrierungszustände für "Home/Roam":

-   Home: registriert im Heimnetzwerk
-   Partner: Registriert in einem Netzwerk, das eng mit dem Heimnetzwerk verbunden ist
-   Nicht-Partner: Registriert in einem Netzwerk, das nicht eng mit dem Heimnetzwerk verbunden ist

Die genaue Bedeutung von "Partner" variiert je nach Netzwerk, stellt aber eine engere Beziehung mit günstigeren Raten dar als ein Nichtpartner. Dies kann der Fall sein, wenn ein regional basierter Operator über eine geschäftliche Anordnung verfügt, um das Funkzugriffsnetzwerk eines anderen Betreibers außerhalb seines Heimbereichs zu verwenden. Sie kann auch den Unterschied zwischen dem Roaming innerhalb einer Region (z. B. EU) und außerhalb der Region darstellen.

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

Der **einfache RoamApplicabilityType-Typ** definiert die folgenden Werte.


| Wert | BESCHREIBUNG | 
|-------|-------------|
| NonPartnerOnly | <p>Dieses Profil wird nur beim Roaming in einem Nicht-Partnernetzwerk verwendet.</p> | 
| PartnerOnly | <p>Dieses Profil wird nur beim Roaming in einem Partnernetzwerk verwendet.</p> | 
| HomeOnly | <p>Dieses Profil wird nur verwendet, wenn es sich um ein Heimnetzwerk handelt.</p> | 
| HomeAndPartner | <p>Dieses Profil wird nur zu Hause oder in einem Partnernetzwerk verwendet.</p> | 
| PartnerAndNonpartner | <p>Dieses Profil wird verwendet, wenn es nicht zu Hause ist (Roaming in einem beliebigen Netzwerk).</p> | 
| AllRoaming | <p>Dieses Profil wird in allen Netzwerken verwendet.</p> | 


 

 



