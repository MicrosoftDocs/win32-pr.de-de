---
description: Mbnprofileext \/ ... \/ Userlogonkred (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 12a65d91-1917-49d4-9b58-68c60464c857
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3f6999763e82051fa30af6109c3a04ae8dc65f77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343322"
---
# <a name="span-idwwan_profile_v4element_userlogoncredspanmbnprofileextuserlogoncred-v4"></a><span data-ttu-id="63c64-103"><span id="WWAN_profile_v4.element_UserLogonCred"></span>Mbnprofileext \/ ... \/ Userlogonkred (v4)</span><span class="sxs-lookup"><span data-stu-id="63c64-103"><span id="WWAN_profile_v4.element_UserLogonCred"></span>MBNProfileExt\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="63c64-104">Anmelde Informationen für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="63c64-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="63c64-105">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="63c64-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="63c64-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="63c64-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="63c64-107">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="63c64-107">Key</span></span>

<span data-ttu-id="63c64-108">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="63c64-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="63c64-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="63c64-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="63c64-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="63c64-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="63c64-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="63c64-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="63c64-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63c64-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63c64-113">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="63c64-113">Child Element</span></span></th>
<th><span data-ttu-id="63c64-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63c64-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63c64-115"><a href="element-ignorepassword.md">Ignorepassword</a></span><span class="sxs-lookup"><span data-stu-id="63c64-115"><a href="element-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="63c64-116">Gibt an, wie Kenn Wörter beim Aktualisieren von Profilen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="63c64-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="63c64-117">Wenn diese Einstellung auf " <strong>true</strong> " festgelegt ist und zum Zeitpunkt des Aktualisierungs Vorgangs ein Profil mit demselben Namen vorhanden ist, wird das Kennwort aus diesem Profil übernommen und im neuen Profil gespeichert.</span><span class="sxs-lookup"><span data-stu-id="63c64-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="63c64-118">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>ignorepassword</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="63c64-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63c64-119"><a href="element-password.md">Kennwort</a></span><span class="sxs-lookup"><span data-stu-id="63c64-119"><a href="element-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="63c64-120">Gibt das Kennwort an, das zum Authentifizieren eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63c64-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="63c64-121">Weitere Informationen finden Sie in der Dokumentation für das v1-Kenn <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Wort</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="63c64-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63c64-122"><a href="element-username.md">UserName</a></span><span class="sxs-lookup"><span data-stu-id="63c64-122"><a href="element-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="63c64-123">Der Benutzername, der für die Anmeldung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63c64-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="63c64-124">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>username</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="63c64-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="63c64-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63c64-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63c64-126">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="63c64-126">Parent Element</span></span></th>
<th><span data-ttu-id="63c64-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63c64-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63c64-128"><a href="element-context.md">Context</a></span><span class="sxs-lookup"><span data-stu-id="63c64-128"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="63c64-129">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="63c64-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="63c64-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63c64-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63c64-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="63c64-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



