---
description: Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Hex (SSID)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368120"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="0d0b8-103">Hex (SSID)-Element</span><span class="sxs-lookup"><span data-stu-id="0d0b8-103">hex (SSID) Element</span></span>

<span data-ttu-id="0d0b8-104">Das Hex (SSID)-Element enthält die SSID eines drahtlosen LANs im Hexadezimal Format.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
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
```

<span data-ttu-id="0d0b8-105">Das-Element wird durch das [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0b8-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d0b8-106">Remarks</span></span>

<span data-ttu-id="0d0b8-107">Obwohl das **Hex** -Element und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element optional sind, muss mindestens ein **Hex** -oder [**Name**](wlan-profileschema-name-ssid-element.md) -Element als untergeordnetes Element des [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="0d0b8-108">Wenn Profilinformationen in eine SSID konvertiert werden, wird das **Hex** -Element in die SSID (sofern vorhanden) konvertiert, und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="0d0b8-109">Wenn das **Hex** -Element nicht vorhanden ist, wird das [**Name**](wlan-profileschema-name-ssid-element.md) -Element mithilfe der Unicode-in-ASCII-Konvertierung in eine SSID konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="0d0b8-110">Wenn eine SSID in einem Profil gespeichert wird, wird das **Hex** -Element immer generiert.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="0d0b8-111">Das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird nur generiert, wenn sowohl die ASCII-als auch die Unicode-Konvertierung der SSID und die Generierung des XML-Profils erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="0d0b8-112">Einige Informationen aus der ursprünglichen SSID können verloren gehen, wenn Sie in einen [**Namen**](wlan-profileschema-name-ssid-element.md)konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="0d0b8-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0d0b8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d0b8-113">Examples</span></span>

<span data-ttu-id="0d0b8-114">Ein Beispiel Profil, das das **Hex** -Element verwendet, finden Sie unter Beispiel für ein Beispiel für den [PPS-Profil](fips-profile-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0d0b8-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0b8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d0b8-115">Requirements</span></span>



| <span data-ttu-id="0d0b8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d0b8-116">Requirement</span></span> | <span data-ttu-id="0d0b8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0d0b8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0d0b8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d0b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0b8-119">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d0b8-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0d0b8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d0b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0b8-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d0b8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="0d0b8-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0d0b8-122">Redistributable</span></span><br/>          | <span data-ttu-id="0d0b8-123">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="0d0b8-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0d0b8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d0b8-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d0b8-125">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="0d0b8-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0d0b8-126">**SSID**</span><span class="sxs-lookup"><span data-stu-id="0d0b8-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="0d0b8-127">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="0d0b8-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0d0b8-128">**SSID (ssidconfig)**</span><span class="sxs-lookup"><span data-stu-id="0d0b8-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




