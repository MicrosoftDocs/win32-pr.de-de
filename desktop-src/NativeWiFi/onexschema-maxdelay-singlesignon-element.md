---
description: Gibt die maximale Verzögerung (in Sekunden) an, bevor der einmalige Anmelde Verbindungsversuch fehlschlägt.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: MaxDelay-Element (SingleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864812"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="4aa30-103">MaxDelay-Element (SingleSignOn)</span><span class="sxs-lookup"><span data-stu-id="4aa30-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="4aa30-104">Das MaxDelay-Element (SingleSignOn) gibt die maximale Verzögerung (in Sekunden) an, bevor der einmalige Anmelde Verbindungsversuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="4aa30-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="4aa30-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4aa30-105">This element is optional.</span></span> <span data-ttu-id="4aa30-106">Wenn MaxDelay nicht in einem Profil angegeben ist, wird ein Wert von 10 Sekunden verwendet.</span><span class="sxs-lookup"><span data-stu-id="4aa30-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="4aa30-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4aa30-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="4aa30-108">Das **MaxDelay** -Element wird durch das [**SingleSignOn**](onexschema-singlesignon-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4aa30-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa30-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aa30-109">Remarks</span></span>

<span data-ttu-id="4aa30-110">Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4aa30-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="4aa30-111">Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4aa30-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa30-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4aa30-112">Requirements</span></span>



| <span data-ttu-id="4aa30-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4aa30-113">Requirement</span></span> | <span data-ttu-id="4aa30-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4aa30-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4aa30-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4aa30-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa30-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aa30-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4aa30-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4aa30-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa30-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4aa30-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4aa30-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aa30-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="4aa30-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4aa30-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4aa30-121">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="4aa30-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="4aa30-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4aa30-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4aa30-123">**SingleSignOn (Onex)**</span><span class="sxs-lookup"><span data-stu-id="4aa30-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
