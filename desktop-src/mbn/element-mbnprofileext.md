---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9167561aabe151b75a4aa295a1c8aacec974df
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884080"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

Das **MBNProfileExt-Element** ist eine Erweiterung des früheren MBNProfile-Elements. Es identifiziert ein Mobile Broadband-Profil mit einem vielfältigeren Satz von Optionen als das MBNProfile-Element.

Es kann mehrere MbnProfileExt-Elemente in einem Profil geben, die Profileinstellungen für einen bestimmten Satz von Betriebsbedingungen beschreiben. Verwenden Sie [**das untergeordnete ProfileConditionedOn-Element**](element-profileconditionedon.md) von **MBNProfileExt,** um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.

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
| <a href="element-adminroamcontrol.md">AdminRoamControl</a> | <p>Gibt an, ob das Profil verwaltungsgesteuert roaminggesteuert ist. Dieses Element ist neu für v4. Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamControlType-Wert.</strong></a> Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>AllRoamAllowed</strong> der Standardwert.</p> | 
| <a href="element-apnid.md">ApnID</a> | <p>Eine diesem Profil zugeordnete APN-ID. Dieses Element ist neu in v4 und optional.</p> | 
| <a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a> | <p>Gibt an, ob das mobile Breitbandgerät automatisch eine Verbindung mit einem Netzwerk herstellen soll.</p><p>Weitere Informationen finden Sie in der Dokumentation zum v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet-Element.</strong></a></p> | 
| <a href="element-connectionmode.md">ConnectionMode</a> | <p>Gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitbandgerät verwendet werden soll.</p><p>Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode-Element</strong></a> v1.</p> | 
| <a href="element-context.md">Context</a> | <p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p> | 
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Gibt eine Liste der bevorzugten Netzwerkanbieter beim Roaming an.</p><p>Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners-Element</strong></a> v1.</p> | 
| <a href="element-description.md">Beschreibung</a> | <p>Eine Beschreibung des Profils.</p> | 
| <a href="element-homeprovidername.md">HomeProviderName</a> | <p>Der Name des Homeanbieters für die bestimmte SIM/das Gerät. Weitere Informationen finden Sie in der Dokumentation zum v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName-Element.</strong></a></p> | 
| <a href="element-iconfilepath.md">ICONFilePath</a> | <p>Der Pfad zur Symboldatei für die Verbindung. Die Benutzeroberfläche für die Betriebssystemverbindung zeigt das Symbol an, wenn eine Verbindung mit diesem Profil hergestellt wird.</p><p>Weitere Informationen zur Verwendung dieses Elements finden Sie in der v1-Dokumentation für <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</p> | 
| <a href="element-isdefault.md">IsDefault</a> | <p>Gibt an, ob dieses Profil das Standardprofil ist.</p><p>Weitere Informationen zu diesem Element finden Sie in der v1-Dokumentation für <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p> | 
| <a href="element-isexclusivetoother.md">IsExclusiveToOther</a> | <p>Gibt an, dass dieses Profil für andere Profile desselben Profils exklusiv ist. Dieses Element ist neu für v4.</p> | 
| <a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a> | <p>Gibt an, dass dieses Profil ein langfristiges zusätzliches PDP-Kontextprofil ist. Wenn der Wert dieses Elements <strong>true ist,</strong>muss <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> ebenfalls auf true festgelegt <strong>werden.</strong> Dies ist ein neues Element für v4.</p> | 
| <a href="element-isprovisioningprofile.md">IsProvisioningProfile</a> | <p>Gibt an, dass dieses Profil nur für die Bereitstellung verwendet werden soll. Andernfalls ist das Profil nicht anwendbar und kann nicht zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden. Dieses Element ist neu für v4.</p><p>Wenn <strong>IsProvisioningProfile</strong> true ist, <a href="element-isdefault.md"><strong>muss IsDefault</strong></a> false und <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> manuell sein.</p> | 
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</p><p>Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil die folgenden Einstellungen aufweisen.</p><ul><li>Das <a href="element-name.md"><strong>Name-Element</strong></a> muss einen systemweiten eindeutigen Namen enthalten.</li><li><a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType muss</strong></a> auf <strong>UserProvisioned festgelegt werden.</strong></li><li>Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID muss</strong></a> die SIM-ID der SIM enthalten, für die dieses Profil vorgesehen ist.</li><li>Der <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode muss</strong></a> auf Manual <strong>festgelegt werden.</strong></li><li>Die <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid muss</strong></a> die GUID für die MMS-Zweckgruppe enthalten.</li><li>Das <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> muss auf true festgelegt <strong>werden.</strong></li></ul> | 
| <a href="element-name.md">Name</a> | <p>Der Name des Profils. Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-name-mbnprofile-element.md"><strong>v1-Element Name.</strong></a></p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</p><p>Dieses Element ist neu für v4. Sie können mehrere Profile angeben, die unter verschiedenen Bedingungen gelten, und das richtige Profil automatisch verwenden, wenn es anwendbar ist. Dieses Element ist optional. Wenn Sie es nicht angeben, ist das Profil immer in Bezug auf die aufgeführten Bedingungen anwendbar.</p> | 
| <a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a> | <p>Gibt den Ersteller des Profils an.</p><p>Weitere Informationen zu diesem Element finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType-Element.</strong></a></p> | 
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Eine optionale Liste von Profilgruppen, wobei jede Gruppe Profile enthält, die für einen gemeinsamen Zweck verwendet werden.</p><p>Dieses Element ist neu für v4 des Schemas.</p><p>Ein Profil kann in mehreren Gruppen aufgeführt werden.</p> | 
| <a href="element-simiccid.md">SimIccID</a> | <p>Die SIM-Identifikationsnummer für GSM-Geräte. Weitere Informationen finden Sie in der Dokumentation für das <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID-Element</strong></a> v1.</p> | 
| <a href="element-subscriberid.md">Subscriberid</a> | <p>Identifiziert den eindeutigen Bezeichner des Profils.</p><p>Für ein GSM-Netzwerk sollte dieses das IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte die MIN (Mobile Identification Number) des Geräts enthalten.</p><p>Weitere Informationen finden Sie in der Dokumentation zum v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID-Element.</strong></a></p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente

Dieses äußerste Element (Dokument) darf nicht in anderen Elementen enthalten sein.

## <a name="requirements"></a>Requirements (Anforderungen)


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
