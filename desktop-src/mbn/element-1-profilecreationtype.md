---
description: ProfileCreationType (in ModemDMConfigProfile)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (in ModemDMConfigProfile)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650465244fca041efcdaa53b737074f70536edc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986433"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)

Gibt an, wie dieses Modem-DM-Profil erstellt wurde.

Dieser Wert wird verwendet, um zu entscheiden, ob ein Benutzer das Profil löschen kann. Benutzer können nur **UserProvisioned-Profile** löschen.

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;ModemDMConfigProfile&gt;](element-modemdmconfigprofile.md)  
**&lt;ProfileCreationType&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>Modem-DM-Konfigurationsprofil.</p> | 


 

## <a name="related-elements"></a>Zugehörige Elemente

Die folgenden Elemente haben denselben Namen wie dieses Element, aber ihr Inhalt oder ihre Attribute sind anders.

-   **[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



