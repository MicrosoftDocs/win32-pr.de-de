---
description: MmscPort
MS-HAID: WWAN\_profile\_v4.element\_MmscPort
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscPort
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab0f0aa319a9768e2ec96ededbf9d9aafc629bcd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480296"
---
# <a name="span-idwwan_profile_v4element_mmscportspanmmscport"></a><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort

Gibt die Portnummer des MMSC-Servers für das Gerät an. Geben Sie 0 an, um anzugeben, dass kein bestimmter Port angegeben ist. Optional.

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscPort>**

## <a name="syntax"></a>Syntax

``` syntax
<MmscPort>

  [TBD (missing description)]

</MmscPort>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</p><p>Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil die folgenden Einstellungen aufweisen.</p><ul><li>Das <a href="element-name.md"><strong>Name-Element</strong></a> muss einen systemweiten eindeutigen Namen enthalten.</li><li><a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType muss</strong></a> auf <strong>UserProvisioned festgelegt werden.</strong></li><li>Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID muss</strong></a> die SIM-ID der SIM enthalten, für die dieses Profil vorgesehen ist.</li><li>Der <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode muss</strong></a> auf Manual <strong>festgelegt werden.</strong></li><li>Die <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid muss</strong></a> die GUID für die MMS-Zweckgruppe enthalten.</li><li>Das <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> muss auf true festgelegt <strong>werden.</strong></li></ul> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
