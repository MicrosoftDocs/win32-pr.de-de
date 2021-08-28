---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6612ce37bfa39b9498b6db4b9ce49cb06a6326
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982133"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration

Konfigurationsinformationen für Multimedia Messaging Service (MMS).

Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil die folgenden Einstellungen aufweisen.

-   Das [**Name-Element**](element-name.md) muss einen systemweit eindeutigen Namen enthalten.
-   [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) muss auf **UserProvisioned** festgelegt werden.
-   Die [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) muss die MUSTID der SIM enthalten, für die dieses Profil vorgesehen ist.
-   [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) muss auf **Manuell** festgelegt werden.
-   [**PurposeGroupGuid**](element-purposegroupguid.md) muss die GUID für die MMS-Zweckgruppe enthalten.
-   [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) muss auf **true** festgelegt werden.

## <a name="element-hierarchy"></a>Elementhierarchie

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;MmsConfiguration&gt;**

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
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>Das <strong>MBNProfileExt-Element</strong> ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein mobiles Breitbandprofil mit einem umfangreicheren Satz von Optionen als das MBNProfile-Element.</p><p>Ein Profil kann mehrere MbnProfileExt-Elemente enthalten, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn-Element</strong></a> von <strong>MBNProfileExt,</strong> um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p> | 


 

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
