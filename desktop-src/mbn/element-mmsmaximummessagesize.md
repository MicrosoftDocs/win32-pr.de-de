---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e20af3d38a594158586247a9798be98c0d97a65b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988673"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize

Gibt die maximale Größe von MMS-Nachrichten in Kilobyte an. Optional.

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;MmsConfiguration&gt;](element-mmsconfiguration.md)  
**&lt;MmsMaximumMessageSize&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
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


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
