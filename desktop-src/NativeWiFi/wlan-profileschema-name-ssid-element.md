---
description: Enthält die SSID eines drahtlosen LANs.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Name (SSID)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867279"
---
# <a name="name-ssid-element"></a><span data-ttu-id="d6b65-103">Name (SSID)-Element</span><span class="sxs-lookup"><span data-stu-id="d6b65-103">name (SSID) Element</span></span>

<span data-ttu-id="d6b65-104">Das Name (SSID)-Element enthält die SSID eines drahtlosen LANs.</span><span class="sxs-lookup"><span data-stu-id="d6b65-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
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
```

<span data-ttu-id="d6b65-105">Das-Element wird durch das [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="d6b65-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6b65-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6b65-106">Remarks</span></span>

<span data-ttu-id="d6b65-107">Bei Namen wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d6b65-107">Names are case-sensitive.</span></span>

<span data-ttu-id="d6b65-108">Obwohl das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element und das **Name** -Element optional sind, muss mindestens ein **Hex** -oder **Name** -Element als untergeordnetes Element des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6b65-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="d6b65-109">Wenn Profilinformationen in eine SSID konvertiert werden, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element in die SSID (sofern vorhanden) konvertiert, und das **Name** -Element wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d6b65-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="d6b65-110">Wenn das **Hex** -Element nicht vorhanden ist, wird das **Name** -Element mithilfe der Unicode-in-ASCII-Konvertierung in eine SSID konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d6b65-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="d6b65-111">Wenn eine SSID in einem Profil gespeichert wird, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element immer generiert.</span><span class="sxs-lookup"><span data-stu-id="d6b65-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="d6b65-112">Das **Name** -Element wird nur generiert, wenn sowohl die ASCII-als auch die Unicode-Konvertierung der SSID und die Generierung des XML-Profils erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="d6b65-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="d6b65-113">Einige Informationen aus der ursprünglichen SSID können verloren gehen, wenn Sie in einen **Namen** konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6b65-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="d6b65-114">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** XML-Escapezeichen, wie z. b. &, werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6b65-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="d6b65-115">Vermeiden Sie die Verwendung von XML-Escapezeichen in SSID-Namen für Profile, die unter Windows XP mit SP3 und Wireless LAN API für Windows XP SP2 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6b65-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="d6b65-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6b65-116">Examples</span></span>

<span data-ttu-id="d6b65-117">Beispiel Profile, die das **Name** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d6b65-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b65-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6b65-118">Requirements</span></span>



| <span data-ttu-id="d6b65-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6b65-119">Requirement</span></span> | <span data-ttu-id="d6b65-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d6b65-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d6b65-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6b65-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6b65-122">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6b65-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6b65-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6b65-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6b65-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6b65-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d6b65-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d6b65-125">Redistributable</span></span><br/>          | <span data-ttu-id="d6b65-126">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="d6b65-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d6b65-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6b65-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6b65-128">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d6b65-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d6b65-129">**SSID**</span><span class="sxs-lookup"><span data-stu-id="d6b65-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="d6b65-130">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="d6b65-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d6b65-131">**SSID (ssidconfig)**</span><span class="sxs-lookup"><span data-stu-id="d6b65-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




