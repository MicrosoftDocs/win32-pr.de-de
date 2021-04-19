---
description: Mbnprofileext- \/ Kontext (v4)
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
ms.openlocfilehash: 8ec231b5d7e2769d86262864e0b9a53621c36a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348169"
---
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span id="WWAN_profile_v4.element_Context"></span>Mbnprofileext- \/ Kontext (v4)

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
<td><a href="element-accessstring.md">AccessString</a></td>
<td><p>Identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.</p>
<p>Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>accessstring</strong></a> -Element.</p></td>
</tr>
<tr class="even">
<td><a href="element-authprotocol.md">AuthProtocol</a></td>
<td><p>>Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.</p>
<p>Beachten Sie, dass in v4 ein neuer-Enumerationswert für dieses Element verfügbar ist. <strong>Autoselection</strong> bedeutet, dass ein Authentifizierungsprotokoll von niedrigeren Ebenen ausgewählt werden muss.</p>
<p>Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>authprotocol</strong></a> -Element.</p></td>
</tr>
<tr class="odd">
<td><a href="element-compression.md">Komprimierung</a></td>
<td><p>Gibt an, ob die Komprimierung im Daten Link für Header und Datenübertragung verwendet wird.</p>
<p>Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-compression-contexttype-element.md"><strong>Komprimierungs</strong></a> Element.</p></td>
</tr>
<tr class="even">
<td><a href="element-iptype.md">Iptype</a></td>
<td><p>Gibt den IP-Typ an, der für diese Datenverbindung verwendet werden soll.</p>
<p>Dieses Element ist neu in v4 des Schemas. Das-Element kann einen der folgenden Werte aufweisen.</p>
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
<td>Der IP-Typ muss von niedrigeren Ebenen ausgewählt werden.</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>IPv4 verwenden</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>IPv6 verwenden</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Verwenden Sie IPv4 und/oder IPv6 als verfügbar.</td>
</tr>
<tr class="odd">
<td>Xlat</td>
<td>Verwenden von 464xlat zum Tunneln von IPv4 über IPv6-Netzwerke</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-userlogoncred.md">UserLogonCred</a></td>
<td><p>Anmelde Informationen für eine Verbindung.</p></td>
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
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Modem-DM-Konfigurations Profil.</p></td>
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

 

 



