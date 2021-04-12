---
description: "\"Fidemdmconfigprofile\" \\/ ... \\/ Authprotocol (v4)"
MS-HAID: WWAN\_profile\_v4.element\_1\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AuthProtocol
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5e6c5a25-fe9e-4d0a-8b5b-4ff585f562af
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7a935d7367589a3043fdd9d064935d0c0dd64b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526051"
---
# <a name="span-idwwan_profile_v4element_1_authprotocolspanmodemdmconfigprofileauthprotocol-v4"></a><span data-ttu-id="e5442-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>"Fidemdmconfigprofile" \/ ... \/ Authprotocol (v4)</span><span class="sxs-lookup"><span data-stu-id="e5442-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>ModemDMConfigProfile\/...\/AuthProtocol (v4)</span></span>

><span data-ttu-id="e5442-104">Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5442-104">Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="e5442-105">Beachten Sie, dass in v4 ein neuer-Enumerationswert für dieses Element verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e5442-105">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="e5442-106">**Autoselection** bedeutet, dass ein Authentifizierungsprotokoll von niedrigeren Ebenen ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e5442-106">**AutoSelection** means that an auth protocol is to be picked by lower layer(s).</span></span>

<span data-ttu-id="e5442-107">Weitere Informationen finden Sie in der Dokumentation für das v1 [**authprotocol**](./schema-authprotocol-contexttype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="e5442-107">For further information, see the documentation for the v1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e5442-108">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="e5442-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a><span data-ttu-id="e5442-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5442-109">Syntax</span></span>

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e5442-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e5442-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e5442-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="e5442-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e5442-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5442-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e5442-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5442-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="e5442-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5442-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e5442-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5442-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5442-116">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e5442-116">Parent Element</span></span></th>
<th><span data-ttu-id="e5442-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5442-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5442-118"><a href="element-1-context.md">Context</a></span><span class="sxs-lookup"><span data-stu-id="e5442-118"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="e5442-119">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e5442-119">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e5442-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5442-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5442-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5442-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
