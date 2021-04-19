---
description: Abonnement-ID
MS-HAID: WWAN\_profile\_v4.element\_SubscriberID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Abonnement-ID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525cd75dbf1ab752ab17ea32d566e57977ab74a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348769"
---
# <a name="span-idwwan_profile_v4element_subscriberidspansubscriberid"></a><span data-ttu-id="725ef-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="725ef-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span></span>

<span data-ttu-id="725ef-104">Identifiziert den eindeutigen Bezeichner des Profils.</span><span class="sxs-lookup"><span data-stu-id="725ef-104">Identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="725ef-105">Bei einem GSM-Netzwerk sollte dies die IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte enthalten, die den minimalen (mobilen Identifikationsnummer) des Geräts enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="725ef-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="725ef-106">Weitere Informationen finden Sie in der Dokumentation zum [**abonniert**](./schema-subscriberid-mbnprofile-element.md) -Element von v1.</span><span class="sxs-lookup"><span data-stu-id="725ef-106">For more information, see the documentation for the v1 [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="725ef-107">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="725ef-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<SubscriberID>**

## <a name="syntax"></a><span data-ttu-id="725ef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="725ef-108">Syntax</span></span>

``` syntax
<SubscriberID>

  subscriberIdType

</SubscriberID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="725ef-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="725ef-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="725ef-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="725ef-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="725ef-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="725ef-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="725ef-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="725ef-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="725ef-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="725ef-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="725ef-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="725ef-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="725ef-115">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="725ef-115">Parent Element</span></span></th>
<th><span data-ttu-id="725ef-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="725ef-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="725ef-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="725ef-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="725ef-118">Das <strong>mbnprofileext</strong> -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="725ef-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="725ef-119">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="725ef-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="725ef-120">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="725ef-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="725ef-121">Verwenden Sie das untergeordnete <a href="element-profileconditionedon.md"><strong>profileconditionedon</strong></a> -Element von <strong>mbnprofileext</strong> , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="725ef-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="725ef-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="725ef-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="725ef-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="725ef-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
