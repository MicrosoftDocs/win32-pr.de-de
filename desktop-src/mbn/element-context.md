---
description: MBNProfileExt-Kontext \/ (v4)
MS-HAID: WWAN\_profile\_v4.element\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Kontext
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eff61884-1d37-4e1a-85f0-2fadf14227ac
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fa14cd19e5502c227d1f7f0814966959680dfe20
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624116"
---
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span id="WWAN_profile_v4.element_Context"></span>MBNProfileExt-Kontext \/ (v4)

Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.

## <a name="element-hierarchy"></a>Elementhierarchie

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Syntax

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a>Schlüssel

`?`   optional (null oder eins)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Untergeordnetes Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-accessstring.md">AccessString</a></td>
<td><p>Identifiziert den APN oder die Wählzeichenfolge, der bzw. die zum Herstellen einer Datenverbindung verwendet werden soll.</p>
<p>Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString-Element</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-authprotocol.md">AuthProtocol</a></td>
<td><p>>Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.</p>
<p>Beachten Sie, dass in v4 ein neuer Enumerationswert für dieses Element verfügbar ist. <strong>AutoSelection bedeutet,</strong> dass ein Authentifizierungsprotokoll von niedrigeren Ebenen ausgewählt werden soll.</p>
<p>Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>v1-AuthProtocol-Element.</strong></a></p></td>
</tr>
<tr class="odd">
<td><a href="element-compression.md">Komprimierung</a></td>
<td><p>Gibt an, ob die Komprimierung am Datenlink für Header und Datenübertragung verwendet wird.</p>
<p>Weitere Informationen finden Sie in der <a href="../mbn/schema-compression-contexttype-element.md"><strong></strong></a> Dokumentation zum Komprimierungselement v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-iptype.md">IPType</a></td>
<td><p>Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.</p>
<p>Dieses Element ist neu in v4 des Schemas. Das -Element kann einen der folgenden Werte haben.</p>
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Standard</td>
<td>Der IP-Typ muss von einer niedrigeren Ebene(n)</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>Verwenden von IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>IPv6 verwenden</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Verwenden Sie IPv4 und/oder IPv6, wie verfügbar.</td>
</tr>
<tr class="odd">
<td>XLAT</td>
<td>Verwenden von 464XLAT zum Tunneln von IPv4 über IPv6-Netzwerke</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-userlogoncred.md">UserLogonCred</a></td>
<td><p>Anmeldeinformationen für eine Verbindung.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Übergeordnetes Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>Das <strong>MBNProfileExt-Element</strong> ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein Mobile Broadband-Profil mit einem vielfältigeren Satz von Optionen als das MBNProfile-Element.</p>
<p>Es kann mehrere MbnProfileExt-Elemente in einem Profil geben, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie <a href="element-profileconditionedon.md"><strong>das untergeordnete ProfileConditionedOn-Element</strong></a> von <strong>MBNProfileExt,</strong> um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Modem-DM-Konfigurationsprofil.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requirements (Anforderungen)

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



