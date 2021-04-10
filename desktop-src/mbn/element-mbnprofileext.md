---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343779"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>Mbnprofileext

Das **mbnprofileext** -Element ist eine Erweiterung des früheren mbnprofile-Elements. Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.

Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt. Verwenden Sie das untergeordnete [**profileconditionedon**](element-profileconditionedon.md) -Element von **mbnprofileext** , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.

## <a name="element-hierarchy"></a>Elementhierarchie

**<MBNProfileExt>**

## <a name="syntax"></a>Syntax

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a>Schlüssel

`?`   optional (0 (null) oder eins)

`*`   optional (0 (null) oder mehr)

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
<td><a href="element-adminenable.md">Adminenable</a></td>
<td><p>Gibt an, ob das Profil administrativ aktiviert ist. Dies ist ein neues Element für v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-adminroamcontrol.md">Adminroamcontrol</a></td>
<td><p>Gibt an, ob das Profil administrativ durchlaufen wird. Dieses Element ist neu für v4. Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamcontroltype</strong></a> -Wert. Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>allroamallowed</strong> der Standardwert.</p></td>
</tr>
<tr class="odd">
<td><a href="element-apnid.md">Apnid</a></td>
<td><p>Eine APN-ID, die diesem Profil zugeordnet ist. Dieses Element ist neu in v4 und optional.</p></td>
</tr>
<tr class="even">
<td><a href="element-autoconnectoninternet.md">Autoconnectoninternet</a></td>
<td><p>Hiermit wird angegeben, ob das mobile Breitband Gerät automatisch eine Verbindung mit einem Netzwerk herstellt.</p>
<p>Weitere Informationen finden Sie in der Dokumentation zum Element " <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>autoconnectoninternet</strong></a> " von v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-connectionmode.md">ConnectionMode</a></td>
<td><p>Gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitband Gerät verwendet werden soll.</p>
<p>Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> -Element.</p></td>
</tr>
<tr class="even">
<td><a href="element-context.md">Context</a></td>
<td><p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Gibt eine Liste der bevorzugten Netzwerkanbieter beim Roaming an.</p>
<p>Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>dataroamingpartners</strong></a> -Element.</p></td>
</tr>
<tr class="even">
<td><a href="element-description.md">Beschreibung</a></td>
<td><p>Eine Beschreibung des Profils.</p></td>
</tr>
<tr class="odd">
<td><a href="element-homeprovidername.md">HomeProviderName</a></td>
<td><p>Der Name des Basis Anbieters für das angegebene SIM/Gerät. Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>homeprovidername</strong></a> -Element.</p></td>
</tr>
<tr class="even">
<td><a href="element-iconfilepath.md">Iconfilepath</a></td>
<td><p>Der Pfad zur Symbol Datei für die Verbindung. Die Benutzeroberfläche für die Betriebssystem Verbindung zeigt das Symbol an, wenn eine Verbindung mit diesem Profil hergestellt wird.</p>
<p>Weitere Informationen zur Verwendung dieses Elements finden Sie in der v1-Dokumentation für <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>iconfilepath</strong></a>.</p></td>
</tr>
<tr class="odd">
<td><a href="element-isdefault.md">IsDefault</a></td>
<td><p>Gibt an, ob dieses Profil das Standardprofil ist.</p>
<p>Weitere Details zu diesem Element finden Sie in der v1-Dokumentation für <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p></td>
</tr>
<tr class="even">
<td><a href="element-isexclusivetoother.md">Isexclusivean other</a></td>
<td><p>Gibt an, dass dieses Profil für andere Profile desselben Profil Satzes exklusiv ist. Dieses Element ist neu für v4.</p></td>
</tr>
<tr class="odd">
<td><a href="element-islongstandingadditionalpdpcontextprofile.md">Islongstandingadditionalpdpcontextprofile</a></td>
<td><p>Gibt an, dass dieses Profil ein langjähriges zusätzliches PDP-Kontext Profil ist. Wenn der Wert dieses Elements " <strong>true</strong>" ist, muss <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>isadditionalpdpcontextprofile</strong></a> ebenfalls auf " <strong>true</strong>" festgelegt werden. Dies ist ein neues Element für v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-isprovisioningprofile.md">Isprovisioningprofile</a></td>
<td><p>Gibt an, dass dieses Profil nur für die Bereitstellung verwendet werden soll. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren. Dieses Element ist neu für v4.</p>
<p>Wenn " <strong>isprovisioningprofile</strong> " auf "true" festgelegt ist, muss " <a href="element-isdefault.md"><strong>IsDefault</strong></a> " den Wert "false" und " <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> "</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmsconfiguration.md">MMSConfiguration</a></td>
<td><p>Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</p>
<p>Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil über die folgenden Einstellungen verfügen.</p>
<ul>
<li>Das <a href="element-name.md"><strong>Name</strong></a> -Element muss einen systemweiten eindeutigen Namen enthalten.</li>
<li>Der <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>profilekreationtype</strong></a> muss auf " <strong>userprovisioned</strong>" festgelegt werden.</li>
<li>Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>simiccid</strong></a> muss die ICCID der SIM enthalten, für die dieses Profil vorgesehen ist.</li>
<li>Der <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> muss auf " <strong>Manual</strong>" festgelegt werden.</li>
<li>Die zugehörige Ziel <a href="element-purposegroupguid.md"><strong>Gruppen-ID</strong></a> muss die GUID für die MMS-Zweck Gruppe enthalten.</li>
<li><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>Isadditionalpdpcontextprofile</strong></a> muss auf " <strong>true</strong>" festgelegt werden.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="element-name.md">Name</a></td>
<td><p>Der Name des Profils. Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-name-mbnprofile-element.md"><strong>namens</strong></a> Element.</p></td>
</tr>
<tr class="odd">
<td><a href="element-profileconditionedon.md">Profileconditionedon</a></td>
<td><p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p>
<p>Dieses Element ist neu für v4. Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unterschiedlichen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie ihn nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</p></td>
</tr>
<tr class="even">
<td><a href="element-profilecreationtype.md">Profilekreationtype (in mbnprofileext)</a></td>
<td><p>Gibt den Ersteller des Profils an.</p>
<p>Weitere Informationen zu diesem Element finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>profilekreationtype</strong></a> -Element.</p></td>
</tr>
<tr class="odd">
<td><a href="element-purposegroups.md">Zielstregruppen</a></td>
<td><p>Eine optionale Liste der Gruppen von Profilen, wobei jede Gruppe Profile enthält, die für einen allgemeinen Zweck verwendet werden.</p>
<p>Dieses Element ist neu für V4 des Schemas.</p>
<p>Ein Profil kann in mehreren Gruppen aufgelistet werden.</p></td>
</tr>
<tr class="even">
<td><a href="element-simiccid.md">Simiccid</a></td>
<td><p>Die SIM-identikations Nummer für GSM-Geräte. Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>simiccid-</strong></a> Element.</p></td>
</tr>
<tr class="odd">
<td><a href="element-subscriberid.md">Abonnement-ID</a></td>
<td><p>Identifiziert den eindeutigen Bezeichner des Profils.</p>
<p>Bei einem GSM-Netzwerk sollte dies die IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte enthalten, die den minimalen (mobilen Identifikationsnummer) des Geräts enthalten soll.</p>
<p>Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>abonniert</strong></a> -Element von v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste (Dokument-) Element darf nicht in anderen Elementen enthalten sein.

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

 

 
