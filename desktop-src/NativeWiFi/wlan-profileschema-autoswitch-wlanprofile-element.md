---
description: Bestimmt das Roamingverhalten eines automatisch verbundenen Netzwerks, wenn ein bevorzugtes Netzwerk in Reichweite ist.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: autoswitch (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863347"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="da177-103">autoswitch (wlanprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="da177-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="da177-104">Das autoswitch (wlanprofile)-Element bestimmt das Roamingverhalten eines automatisch verbundenen Netzwerks, wenn ein bevorzugtes Netzwerk in Reichweite ist.</span><span class="sxs-lookup"><span data-stu-id="da177-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="da177-105">.</span><span class="sxs-lookup"><span data-stu-id="da177-105">.</span></span> <span data-ttu-id="da177-106">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="da177-106">This element is optional.</span></span>

<span data-ttu-id="da177-107">Wenn autoswitch den Wert "true" hat und [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) auf "Auto" festgelegt ist, muss eine Verbindung mit einem besser bevorzugten Netzwerk versucht werden, wenn ein bevorzugtes Netzwerk in den Bereich kommt.</span><span class="sxs-lookup"><span data-stu-id="da177-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="da177-108">Ein bevorzugtes Netzwerk ist ein höheres Netzwerk in der Liste der bevorzugten Drahtlos Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="da177-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="da177-109">Dieser Verbindungsversuch tritt auf, wenn eine Verbindung mit einem anderen Netzwerk besteht.</span><span class="sxs-lookup"><span data-stu-id="da177-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="da177-110">Wenn [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) auf "Auto" festgelegt ist, kann dieser Wert entweder "true" oder "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="da177-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="da177-111">Wenn [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) auf "Manual" festgelegt ist, muss dieser Wert auf "false" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="da177-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="da177-112">Dieses Element hat keine Auswirkung auf ein manuell verbundenes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="da177-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="da177-113">Ein autoswitch-Wert, der auf "true" festgelegt ist, führt zu einer höheren Häufigkeit der regelmäßigen Überprüfung neuer Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="da177-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="da177-114">Dies kann dazu führen, dass regelmäßige Überprüfungen und erhöhter Stromverbrauch durch den Drahtlos Netzwerkadapter verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="da177-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="da177-115">**Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst:** Änderungen werden unter Windows 7 und Windows Server 2008 R2 implementiert, und der drahtlose LAN-Dienst wird installiert, um die Leistung des drahtlos Netzwerks zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="da177-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="da177-116">Diese Änderungen sind so konzipiert, dass die Radiofrequenz Belastung, der Stromverbrauch und die Unterbrechung des Echt Zeit Datenverkehrs über Drahtlos Netzwerke reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="da177-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="da177-117">Die Standardeinstellung für **autoswitch** , wenn dieses Element nicht in einem Drahtlos LAN-Profil festgelegt ist, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="da177-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="da177-118">Die Standardeinstellung wird unter Windows 7 und Windows Server 2008 R2 in "false" geändert, wobei der drahtlose LAN-Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="da177-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="da177-119">Die Standardeinstellung ist auf Windows Server 2008 und Windows Vista auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da177-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="da177-120">Es wird empfohlen, den Wert des **autoswitch** -Elements, das von einer Anwendung in einem WLAN-Profil verwendet wird, auf "false" festzulegen, um die Häufigkeit der regelmäßigen Überprüfung auf neue Netzwerke zu reduzieren, es sei denn, es ist erforderlich, dass eine Anwendung diesen Wert auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da177-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="da177-121">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da177-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="da177-122">Das **autoswitch** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="da177-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="da177-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da177-123">Examples</span></span>

<span data-ttu-id="da177-124">Beispiel Profile, die das **autoswitch** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="da177-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da177-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da177-125">Requirements</span></span>



| <span data-ttu-id="da177-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da177-126">Requirement</span></span> | <span data-ttu-id="da177-127">Wert</span><span class="sxs-lookup"><span data-stu-id="da177-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da177-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da177-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da177-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da177-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da177-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da177-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da177-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da177-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da177-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da177-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="da177-133">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="da177-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="da177-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="da177-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="da177-135">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="da177-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="da177-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="da177-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




