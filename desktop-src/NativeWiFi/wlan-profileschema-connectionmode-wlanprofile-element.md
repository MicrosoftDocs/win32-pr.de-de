---
description: Gibt an, ob die Verbindung mit einem Drahtlos LAN automatisch oder vom Benutzer initiiert werden soll.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: ConnectionMode (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753753"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="d9668-103">ConnectionMode (wlanprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="d9668-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="d9668-104">Das ConnectionMode (wlanprofile)-Element gibt an, ob die Verbindung mit einem Drahtlos LAN automatisch oder vom Benutzer initiiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9668-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="d9668-105">Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf ESS festgelegt ist, kann dieser Wert entweder "Auto" oder "Manual" lauten.</span><span class="sxs-lookup"><span data-stu-id="d9668-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="d9668-106">Der Standardwert ist Auto, wenn dieses Element nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d9668-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="d9668-107">Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf IBSS festgelegt ist, muss dieser Wert manuell lauten.</span><span class="sxs-lookup"><span data-stu-id="d9668-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="d9668-108">Das **ConnectionMode** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="d9668-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9668-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9668-109">Remarks</span></span>

<span data-ttu-id="d9668-110">In der folgenden Tabelle werden die-Enumerationswerte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9668-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="d9668-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d9668-111">Value</span></span>  | <span data-ttu-id="d9668-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9668-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9668-113">auto</span><span class="sxs-lookup"><span data-stu-id="d9668-113">auto</span></span>   | <span data-ttu-id="d9668-114">Die Verbindung mit dem Drahtlos Netzwerk sollte automatisch initiiert werden, wenn das Netzwerk in Reichweite ist.</span><span class="sxs-lookup"><span data-stu-id="d9668-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="d9668-115">manual</span><span class="sxs-lookup"><span data-stu-id="d9668-115">manual</span></span> | <span data-ttu-id="d9668-116">Die Verbindung mit dem Drahtlos Netzwerk wird nur bei der expliziten Anforderung eines Benutzers hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d9668-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="d9668-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9668-117">Examples</span></span>

<span data-ttu-id="d9668-118">Beispiel Profile, die das **ConnectionMode** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d9668-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9668-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9668-119">Requirements</span></span>



| <span data-ttu-id="d9668-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9668-120">Requirement</span></span> | <span data-ttu-id="d9668-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d9668-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d9668-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9668-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d9668-123">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9668-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d9668-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9668-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d9668-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9668-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d9668-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d9668-126">Redistributable</span></span><br/>          | <span data-ttu-id="d9668-127">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="d9668-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d9668-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9668-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9668-129">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d9668-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d9668-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d9668-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d9668-131">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="d9668-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d9668-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d9668-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




