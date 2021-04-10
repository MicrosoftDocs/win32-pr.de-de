---
description: MMSConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MMSConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214561"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MMSConfiguration

Konfigurationsinformationen für den Multimedia Messaging Service (MMS).

Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil über die folgenden Einstellungen verfügen.

-   Das [**Name**](element-name.md) -Element muss einen systemweiten eindeutigen Namen enthalten.
-   Der [**profilekreationtype**](./schema-profilecreationtype-mbnprofile-element.md) muss auf " **userprovisioned**" festgelegt werden.
-   Die [**simiccid**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) muss die ICCID der SIM enthalten, für die dieses Profil vorgesehen ist.
-   Der [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) muss auf " **Manual**" festgelegt werden.
-   Die zugehörige Ziel [**Gruppen-ID**](element-purposegroupguid.md) muss die GUID für die MMS-Zweck Gruppe enthalten.
-   [**Isadditionalpdpcontextprofile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) muss auf " **true**" festgelegt werden.

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

`?`   optional (0 (null) oder eins)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Untergeordnetes Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></td>
<td><p>Gibt die maximale Größe von MMS-Nachrichten in Kilobyte an. Dies ist optional.</p></td>
</tr>
<tr class="even">
<td><a href="element-mmscport.md">MmscPort</a></td>
<td><p>Gibt die Portnummer des MMSC-Servers für das Gerät an. Geben Sie 0 an, um anzugeben, dass kein bestimmter Port angegeben wird. Dies ist optional.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmscurl.md">MmscUrl</a></td>
<td><p>Gibt die URL des MMSC-Servers für das Gerät an. Dies ist optional.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Übergeordnetes Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements. Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</p>
<p>Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt. Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
