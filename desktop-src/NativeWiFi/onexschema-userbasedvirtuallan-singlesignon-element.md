---
description: Gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: userbasedvirtuallan (SingleSignOn)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129732"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="4eec4-103">userbasedvirtuallan (SingleSignOn)-Element</span><span class="sxs-lookup"><span data-stu-id="4eec4-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="4eec4-104">Das userbasedvirtuallan (SingleSignOn)-Element gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4eec4-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="4eec4-105">Einige Netzwerk Zugriffs Server-Geräte (NAS) ändern das VLAN, nachdem sich ein Benutzer authentifiziert hat.</span><span class="sxs-lookup"><span data-stu-id="4eec4-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="4eec4-106">Wenn userbasedvirtuallan den Wert true hat, kann der NAS das VLAN eines Geräts ändern, nachdem sich ein Benutzer authentifiziert hat.</span><span class="sxs-lookup"><span data-stu-id="4eec4-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="4eec4-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4eec4-107">This element is optional.</span></span> <span data-ttu-id="4eec4-108">Wenn userbasedvirtuallan nicht in einem Profil angegeben ist, wird der Wert false verwendet.</span><span class="sxs-lookup"><span data-stu-id="4eec4-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="4eec4-109">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4eec4-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="4eec4-110">Das **userbasedvirtuallan** -Element wird durch das [**SingleSignOn**](onexschema-singlesignon-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4eec4-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eec4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eec4-111">Remarks</span></span>

<span data-ttu-id="4eec4-112">Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eec4-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="4eec4-113">Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4eec4-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4eec4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4eec4-114">Requirements</span></span>



| <span data-ttu-id="4eec4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4eec4-115">Requirement</span></span> | <span data-ttu-id="4eec4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4eec4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4eec4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4eec4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4eec4-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4eec4-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4eec4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4eec4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4eec4-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4eec4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4eec4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eec4-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="4eec4-122">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4eec4-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4eec4-123">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="4eec4-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="4eec4-124">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4eec4-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4eec4-125">**SingleSignOn (Onex)**</span><span class="sxs-lookup"><span data-stu-id="4eec4-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
