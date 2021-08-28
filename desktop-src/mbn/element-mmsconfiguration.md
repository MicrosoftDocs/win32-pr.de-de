---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 843cb0fc67211bec13295a92e467e8358d407312
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480286"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration

Konfigurationsinformationen für den Multimedia Messaging Service (MMS).

Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil die folgenden Einstellungen aufweisen.

-   Das [**Name-Element**](element-name.md) muss einen systemweiten eindeutigen Namen enthalten.
-   [**ProfileCreationType muss**](./schema-profilecreationtype-mbnprofile-element.md) auf **UserProvisioned festgelegt werden.**
-   Die [**SimIccID muss**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) die SIM-ID der SIM enthalten, für die dieses Profil vorgesehen ist.
-   Der [**ConnectionMode muss**](./schema-connectionmode-mbnprofile-element.md) auf Manual **festgelegt werden.**
-   Die [**PurposeGroupGuid muss**](element-purposegroupguid.md) die GUID für die MMS-Zweckgruppe enthalten.
-   Das [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) muss auf true festgelegt **werden.**

## <a name="element-hierarchy"></a>Elementhierarchie

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a>Syntax

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a>Schlüssel

`?`   optional (null oder eins)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente


| Untergeordnetes Element | BESCHREIBUNG | 
|---------------|-------------|
| <a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a> | <p>Gibt die maximale Größe von MMS-Nachrichten in Kilobyte an. Optional.</p> | 
| <a href="element-mmscport.md">MmscPort</a> | <p>Gibt die Portnummer des MMSC-Servers für das Gerät an. Geben Sie 0 an, um anzugeben, dass kein bestimmter Port angegeben ist. Optional.</p> | 
| <a href="element-mmscurl.md">MmscUrl</a> | <p>Gibt die URL des MMSC-Servers für das Gerät an. Optional.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Das <strong>MBNProfileExt-Element</strong> ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein Mobile Broadband-Profil mit einem vielfältigeren Satz von Optionen als das MBNProfile-Element.</p><p>Es kann mehrere MbnProfileExt-Elemente in einem Profil geben, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie <a href="element-profileconditionedon.md"><strong>das untergeordnete ProfileConditionedOn-Element</strong></a> von <strong>MBNProfileExt,</strong> um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
