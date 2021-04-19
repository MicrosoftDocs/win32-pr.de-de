---
description: Ist das Stamm Element, das ein mobiles Breitband Profil identifiziert.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Mbnprofile-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359858"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="0c1ba-103">Mbnprofile-Element</span><span class="sxs-lookup"><span data-stu-id="0c1ba-103">MBNProfile Element</span></span>

<span data-ttu-id="0c1ba-104">Das **mbnprofile** -Element ist das Stamm Element, das ein mobiles Breitband Profil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="0c1ba-105">Es kann nur ein Element dieses Typs pro Dokument vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="0c1ba-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c1ba-106">Child elements</span></span>



| <span data-ttu-id="0c1ba-107">Element</span><span class="sxs-lookup"><span data-stu-id="0c1ba-107">Element</span></span>                                                                          | <span data-ttu-id="0c1ba-108">type</span><span class="sxs-lookup"><span data-stu-id="0c1ba-108">Type</span></span>                                                           | <span data-ttu-id="0c1ba-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c1ba-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="0c1ba-110">**Autoconnectoninternet**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="0c1ba-111">boolean</span><span class="sxs-lookup"><span data-stu-id="0c1ba-111">boolean</span></span>                                                        | <span data-ttu-id="0c1ba-112">Gibt an, ob das Gerät automatisch eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="0c1ba-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="0c1ba-114">Die automatischen Geräte Verbindungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="0c1ba-115">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="0c1ba-116">**contextType**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="0c1ba-117">Setup Parameter für die Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="0c1ba-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="0c1ba-119">Bevorzugte Netzwerkanbieter für Roaming.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="0c1ba-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="0c1ba-121">**nametype**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="0c1ba-122">Beschreibung des Profils.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="0c1ba-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="0c1ba-124">**providernametype**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="0c1ba-125">Der Name des Home-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="0c1ba-126">**Iconfilepath**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="0c1ba-127">**iconfiletype**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="0c1ba-128">Der Pfad zur Symbol Datei.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="0c1ba-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="0c1ba-130">boolean</span><span class="sxs-lookup"><span data-stu-id="0c1ba-130">boolean</span></span>                                                        | <span data-ttu-id="0c1ba-131">Gibt an, ob das Profil das Standardprofil ist.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="0c1ba-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="0c1ba-133">**nametype**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="0c1ba-134">Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="0c1ba-135">**Profilekreationtype**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="0c1ba-136">Informationen zum Ersteller des Profils.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="0c1ba-137">**Simiccid**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="0c1ba-138">**simiccidtype**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="0c1ba-139">SIM-Identifikationsnummer für GSM-Geräte.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="0c1ba-140">**Abonnement-ID**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="0c1ba-141">**Index Type**</span><span class="sxs-lookup"><span data-stu-id="0c1ba-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="0c1ba-142">Eindeutiger Bezeichner des Profils.</span><span class="sxs-lookup"><span data-stu-id="0c1ba-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="0c1ba-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c1ba-143">Requirements</span></span>



| <span data-ttu-id="0c1ba-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c1ba-144">Requirement</span></span> | <span data-ttu-id="0c1ba-145">Wert</span><span class="sxs-lookup"><span data-stu-id="0c1ba-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="0c1ba-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c1ba-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1ba-147">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0c1ba-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="0c1ba-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c1ba-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1ba-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c1ba-149">None supported</span></span><br/>                         |



 

 




