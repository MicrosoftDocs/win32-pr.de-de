---
description: Enthält mindestens eine SSIDs für drahtlose LANs.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Ssidconfig (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865739"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="a599e-103">Ssidconfig (wlanprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="a599e-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="a599e-104">Das ssidconfig (wlanprofile)-Element enthält mindestens eine SSIDs für drahtlose LANs.</span><span class="sxs-lookup"><span data-stu-id="a599e-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
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
            <xs:element name="nonBroadcast"
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

<span data-ttu-id="a599e-105">Das **ssidconfig** -Element wird vom [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="a599e-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a599e-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a599e-106">Child elements</span></span>



| <span data-ttu-id="a599e-107">Element</span><span class="sxs-lookup"><span data-stu-id="a599e-107">Element</span></span>                                                                    | <span data-ttu-id="a599e-108">type</span><span class="sxs-lookup"><span data-stu-id="a599e-108">Type</span></span>                                                              | <span data-ttu-id="a599e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a599e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a599e-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="a599e-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="a599e-111">Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.</span><span class="sxs-lookup"><span data-stu-id="a599e-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a599e-112">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="a599e-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="a599e-113">Enthält den Namen (Groß-/Kleinschreibung) der SSID eines drahtlosen LANs.</span><span class="sxs-lookup"><span data-stu-id="a599e-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="a599e-114">**nicht Broadcast**</span><span class="sxs-lookup"><span data-stu-id="a599e-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="a599e-115">boolean</span><span class="sxs-lookup"><span data-stu-id="a599e-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a599e-116">Gibt an, ob das Netzwerk seine SSID überträgt.</span><span class="sxs-lookup"><span data-stu-id="a599e-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="a599e-117">Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf ESS festgelegt ist, kann dieser Wert entweder **true** oder **false** sein.</span><span class="sxs-lookup"><span data-stu-id="a599e-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="a599e-118">Der Standardwert ist **true** , wenn dieses Element nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a599e-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="a599e-119">Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf IBSS festgelegt ist, muss dieser Wert **false** lauten.</span><span class="sxs-lookup"><span data-stu-id="a599e-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="a599e-120">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a599e-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="a599e-121">**SSID**</span><span class="sxs-lookup"><span data-stu-id="a599e-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="a599e-122">Enthält eine SSID für ein drahtloses LAN.</span><span class="sxs-lookup"><span data-stu-id="a599e-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="a599e-123">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Höchstens ein [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Element kann in einem Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a599e-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="a599e-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a599e-124">Examples</span></span>

<span data-ttu-id="a599e-125">Beispiel Profile, die das **ssidconfig** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a599e-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a599e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a599e-126">Requirements</span></span>



| <span data-ttu-id="a599e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a599e-127">Requirement</span></span> | <span data-ttu-id="a599e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a599e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a599e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a599e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a599e-130">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a599e-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a599e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a599e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a599e-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a599e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a599e-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a599e-133">Redistributable</span></span><br/>          | <span data-ttu-id="a599e-134">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="a599e-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a599e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a599e-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a599e-136">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="a599e-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a599e-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a599e-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a599e-138">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="a599e-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a599e-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a599e-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
