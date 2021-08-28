---
description: ModemDMConfigProfile \/ ... \/ UserLogonCred (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d563cf8-ea40-46b3-a74e-ec7640ca9824
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 270ef6c61bcbb0aad6800177537a8efd4dedf75c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481726"
---
# <a name="span-idwwan_profile_v4element_1_userlogoncredspanmodemdmconfigprofileuserlogoncred-v4"></a><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile \/ ... \/ UserLogonCred (v4)

Anmeldeinformationen für eine Verbindung.

## <a name="element-hierarchy"></a>Elementhierarchie

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a>Syntax

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a>Schlüssel

`?`   optional (null oder eins)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente


| Untergeordnetes Element | BESCHREIBUNG | 
|---------------|-------------|
| <a href="element-1-ignorepassword.md">IgnorePassword</a> | <p>Gibt an, wie Kennwörter beim Aktualisieren von Profilen behandelt werden.</p><p>Wenn auf <strong>TRUE</strong> festgelegt ist und zum Zeitpunkt des Updatevorgangs ein Profil mit dem gleichen Namen vorhanden ist, wird das Kennwort aus diesem Profil verwendet und im neuen Profil gespeichert.</p><p>Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword-Element</strong></a> von v1.</p> | 
| <a href="element-1-password.md">Kennwort</a> | <p>Gibt das Kennwort an, das zum Authentifizieren eines Benutzers verwendet wird.</p><p>Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-password-userlogoncred-element.md"><strong>v1 Password-Element.</strong></a></p> | 
| <a href="element-1-username.md">UserName</a> | <p>Der Benutzername, der für die Anmeldung verwendet werden soll.</p><p>Weitere Informationen finden Sie in der Dokumentation für das <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName-Element</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-1-context.md">Context</a> | <p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



