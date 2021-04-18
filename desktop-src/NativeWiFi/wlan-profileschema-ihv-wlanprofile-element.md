---
description: Enthält verschiedene Einstellungen für unabhängige Hardware Anbieter.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: IHV-Element (wlanprofile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347850"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="22901-103">IHV-Element (wlanprofile)</span><span class="sxs-lookup"><span data-stu-id="22901-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="22901-104">Das IHV (wlanprofile)-Element enthält verschiedene Einstellungen für unabhängige Hardwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="22901-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="22901-105">Wenn ein Profil IHV-Sicherheitseinstellungen enthält, überschreiben Sie von Microsoft definierte Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="22901-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="22901-106">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22901-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
                type="boolean"
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

<span data-ttu-id="22901-107">Das-Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="22901-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="22901-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22901-108">Child elements</span></span>



| <span data-ttu-id="22901-109">Element</span><span class="sxs-lookup"><span data-stu-id="22901-109">Element</span></span>                                                             | <span data-ttu-id="22901-110">type</span><span class="sxs-lookup"><span data-stu-id="22901-110">Type</span></span>                                                              | <span data-ttu-id="22901-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22901-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22901-112">**Stech**</span><span class="sxs-lookup"><span data-stu-id="22901-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="22901-113">Enthält IHV-bezogene Konnektivitätseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="22901-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="22901-114">**Ische**</span><span class="sxs-lookup"><span data-stu-id="22901-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="22901-115">Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.</span><span class="sxs-lookup"><span data-stu-id="22901-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="22901-116">**Ouiheader**</span><span class="sxs-lookup"><span data-stu-id="22901-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="22901-117">Identifiziert den IHV.</span><span class="sxs-lookup"><span data-stu-id="22901-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="22901-118">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="22901-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="22901-119">Enthält IHV-spezifische Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="22901-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="22901-120">Die Sicherheitseinstellungen von Microsoft und die IHV-Sicherheitseinstellungen schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="22901-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="22901-121">Das gesamte Profil ist ungültig, wenn beide Sicherheitseinstellungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="22901-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="22901-122">**Sorte**</span><span class="sxs-lookup"><span data-stu-id="22901-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="22901-123">Enthält eine hexbinär Datei mit 1 Byte, die zur Unterscheidung von NICs durch denselben IHV verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22901-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="22901-124">**usemsonex**</span><span class="sxs-lookup"><span data-stu-id="22901-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="22901-125">boolean</span><span class="sxs-lookup"><span data-stu-id="22901-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="22901-126">Gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22901-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="22901-127">Wenn [**usemsonex**](wlan-profileschema-usemsonex-ihv-element.md) auf true festgelegt ist, verwenden die IHV-Sicherheitskomponenten von Microsoft definierte 802.1 x-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="22901-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="22901-128">Wenn **usemsonex** den Wert false hat, verwenden IHV-Sicherheitskomponenten vom Hersteller bereitgestellte 802.1 x-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="22901-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="22901-129">Standardmäßig ist **usemsonex** false.</span><span class="sxs-lookup"><span data-stu-id="22901-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="22901-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="22901-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="22901-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22901-131">Requirements</span></span>



| <span data-ttu-id="22901-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22901-132">Requirement</span></span> | <span data-ttu-id="22901-133">Wert</span><span class="sxs-lookup"><span data-stu-id="22901-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22901-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22901-134">Minimum supported client</span></span><br/> | <span data-ttu-id="22901-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22901-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22901-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22901-136">Minimum supported server</span></span><br/> | <span data-ttu-id="22901-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22901-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22901-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22901-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="22901-139">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="22901-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="22901-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="22901-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="22901-141">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="22901-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="22901-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="22901-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
