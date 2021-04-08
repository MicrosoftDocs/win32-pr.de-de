---
description: Enthält eine SSID für ein drahtloses LAN.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID-Element (ssidconfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866031"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="e921c-103">SSID-Element (ssidconfig)</span><span class="sxs-lookup"><span data-stu-id="e921c-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="e921c-104">Das SSID-Element (ssidconfig) enthält eine SSID für ein drahtloses LAN.</span><span class="sxs-lookup"><span data-stu-id="e921c-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="e921c-105">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Höchstens ein **SSID** -Element kann in einem Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e921c-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
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
```

<span data-ttu-id="e921c-106">Das **SSID** -Element wird vom [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="e921c-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e921c-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e921c-107">Child elements</span></span>



| <span data-ttu-id="e921c-108">Element</span><span class="sxs-lookup"><span data-stu-id="e921c-108">Element</span></span>                                              | <span data-ttu-id="e921c-109">type</span><span class="sxs-lookup"><span data-stu-id="e921c-109">Type</span></span> | <span data-ttu-id="e921c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e921c-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="e921c-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="e921c-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="e921c-112">Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.</span><span class="sxs-lookup"><span data-stu-id="e921c-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="e921c-113">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="e921c-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="e921c-114">Enthält die SSID für ein drahtloses LAN.</span><span class="sxs-lookup"><span data-stu-id="e921c-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="e921c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e921c-115">Remarks</span></span>

<span data-ttu-id="e921c-116">Obwohl das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element optional sind, muss mindestens ein **Hex** -oder [**Name**](wlan-profileschema-name-ssid-element.md) -Element als untergeordnetes Element des **SSID** -Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e921c-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="e921c-117">Wenn Profilinformationen in eine SSID konvertiert werden, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element in die SSID (sofern vorhanden) konvertiert, und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e921c-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="e921c-118">Wenn das **Hex** -Element nicht vorhanden ist, wird das [**Name**](wlan-profileschema-name-ssid-element.md) -Element mithilfe der Unicode-in-ASCII-Konvertierung in eine SSID konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e921c-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="e921c-119">Wenn eine SSID in einem Profil gespeichert wird, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element immer generiert.</span><span class="sxs-lookup"><span data-stu-id="e921c-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="e921c-120">Das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird nur generiert, wenn sowohl die ASCII-als auch die Unicode-Konvertierung der SSID und die Generierung des XML-Profils erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="e921c-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="e921c-121">Einige Informationen aus der ursprünglichen SSID können verloren gehen, wenn Sie in einen [**Namen**](wlan-profileschema-name-ssid-element.md)konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="e921c-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e921c-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e921c-122">Examples</span></span>

<span data-ttu-id="e921c-123">Beispiel Profile, die das **SSID** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e921c-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e921c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e921c-124">Requirements</span></span>



| <span data-ttu-id="e921c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e921c-125">Requirement</span></span> | <span data-ttu-id="e921c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e921c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e921c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e921c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e921c-128">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e921c-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e921c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e921c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e921c-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e921c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e921c-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e921c-131">Redistributable</span></span><br/>          | <span data-ttu-id="e921c-132">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="e921c-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e921c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e921c-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="e921c-134">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="e921c-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e921c-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="e921c-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="e921c-136">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="e921c-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e921c-137">**Ssidconfig (wlanprofile)**</span><span class="sxs-lookup"><span data-stu-id="e921c-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




