---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf6b821d36fc69c06fd42fad58efc4102e64f6a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987913"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

Das **MBNProfileExt-Element** ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein mobiles Breitbandprofil mit einem umfangreicheren Satz von Optionen als das MBNProfile-Element.

Ein Profil kann mehrere MbnProfileExt-Elemente enthalten, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie das untergeordnete [**ProfileConditionedOn-Element**](element-profileconditionedon.md) von **MBNProfileExt,** um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.

## <a name="element-hierarchy"></a>Elementhierarchie

**&lt;MBNProfileExt&gt;**

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

`?`   optional (null oder eins)

`*`   optional (null oder mehr)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente


| Untergeordnetes Element | BESCHREIBUNG | 
|---------------|-------------|
| <a href="element-adminenable.md">AdminEnable</a> | <p>Gibt an, ob das Profil administratorisch aktiviert ist. Dies ist ein neues Element für v4.</p> | 
| <a href="element-adminroamcontrol.md">AdminRoamControl</a> | <p>Gibt an, ob das Profil vom Administrator per Roaming gesteuert wird. Dieses Element ist neu für v4. Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamControlType-Wert.</strong></a> Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>AllRoamAllowed</strong> der Standardwert.</p> | 
| <a href="element-apnid.md">ApnID</a> | <p>Eine DIESEM Profil zugeordnete APN-ID. Dieses Element ist in v4 neu und optional.</p> | 
| <a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a> | <p>Gibt an, ob das mobile Breitbandgerät automatisch eine Verbindung mit einem Netzwerk herstellt.</p><p>Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>v1 AutoConnectOnInternet-Element.</strong></a></p> | 
| <a href="element-connectionmode.md">ConnectionMode</a> | <p>Gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitbandgerät verwendet werden soll.</p><p>Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode-Element</strong></a> v1.</p> | 
| <a href="element-context.md">Context</a> | <p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p> | 
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Gibt eine Liste der bevorzugten Netzwerkanbieter beim Roaming an.</p><p>Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners-Element</strong></a> v1.</p> | 
| <a href="element-description.md">Beschreibung</a> | <p>Eine Beschreibung des Profils.</p> | 
| <a href="element-homeprovidername.md">HomeProviderName</a> | <p>Der Name des Heimanbieters für die angegebene SIM/das angegebene Gerät. Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName-Element.</strong></a></p> | 
| <a href="element-iconfilepath.md">ICONFilePath</a> | <p>Der Pfad zur Symboldatei für die Verbindung. Die Benutzeroberfläche der Betriebssystemverbindung zeigt das Symbol an, wenn eine Verbindung mit diesem Profil hergestellt wird.</p><p>Weitere Informationen zur Verwendung dieses Elements finden Sie in der v1-Dokumentation für <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath.</strong></a></p> | 
| <a href="element-isdefault.md">IsDefault</a> | <p>Gibt an, ob dieses Profil das Standardprofil ist.</p><p>Weitere Informationen zu diesem Element finden Sie in der v1-Dokumentation für <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p> | 
| <a href="element-isexclusivetoother.md">IsExclusiveToOther</a> | <p>Gibt an, dass dieses Profil ausschließlich für andere Profile derselben Profilsatz(en) gilt. Dieses Element ist neu für v4.</p> | 
| <a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a> | <p>Gibt an, dass dieses Profil ein seit langem bestehendes zusätzliches PDP-Kontextprofil ist. Wenn der Wert dieses Elements <strong>true</strong>ist, muss <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> ebenfalls auf <strong>true</strong>festgelegt werden. Dies ist ein neues Element für v4.</p> | 
| <a href="element-isprovisioningprofile.md">IsProvisioningProfile</a> | <p>Gibt an, dass dieses Profil nur für die Bereitstellung verwendet werden soll. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Dieses Element ist neu für v4.</p><p>Wenn <strong>IsProvisioningProfile</strong> true ist, muss <a href="element-isdefault.md"><strong>IsDefault</strong></a> false und <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> manuell sein.</p> | 
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Konfigurationsinformationen für Multimedia Messaging Service (MMS).</p><p>Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil die folgenden Einstellungen aufweisen.</p><ul><li>Das <a href="element-name.md"><strong>Name-Element</strong></a> muss einen systemweit eindeutigen Namen enthalten.</li><li><a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> muss auf <strong>UserProvisioned</strong>festgelegt werden.</li><li>Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> muss die MUSTID der SIM enthalten, für die dieses Profil vorgesehen ist.</li><li><a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> muss auf <strong>Manuell</strong>festgelegt werden.</li><li><a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> muss die GUID für die MMS-Zweckgruppe enthalten.</li><li><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> muss auf <strong>true</strong>festgelegt werden.</li></ul> | 
| <a href="element-name.md">Name</a> | <p>Der Name des Profils. Weitere Informationen finden Sie in der <a href="../mbn/schema-name-mbnprofile-element.md"><strong></strong></a> Dokumentation für das v1 Name-Element.</p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p><p>Dieses Element ist neu für v4. Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unter verschiedenen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie sie nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</p> | 
| <a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a> | <p>Gibt den Ersteller des Profils an.</p><p>Weitere Informationen zu diesem Element finden Sie in der Dokumentation für das <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>v1 ProfileCreationType-Element.</strong></a></p> | 
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Eine optionale Liste von Gruppen von Profilen, wobei jede Gruppe Profile enthält, die für einen gemeinsamen Zweck verwendet werden.</p><p>Dieses Element ist neu für Version 4 des Schemas.</p><p>Ein Profil kann in mehreren Gruppen aufgelistet werden.</p> | 
| <a href="element-simiccid.md">SimIccID</a> | <p>Die SIM-Identifikationsnummer für GSM-Geräte. Weitere Informationen finden Sie in der Dokumentation für das <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>v1 SimIccID-Element.</strong></a></p> | 
| <a href="element-subscriberid.md">Subscriberid</a> | <p>Identifiziert den eindeutigen Bezeichner des Profils.</p><p>Für ein GSM-Netzwerk sollte dies das IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte die MIN (Mobile Identification Number) des Geräts enthalten.</p><p>Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>v1 SubscriberID-Element.</strong></a></p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste Element (Dokument) darf nicht in anderen Elementen enthalten sein.

## <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
