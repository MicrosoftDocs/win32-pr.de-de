---
description: Gibt Single Sign-on Netzwerk Konfigurationsinformationen (SSO) an.
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: SingleSignOn (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349397"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="102a8-103">SingleSignOn (Onex)-Element</span><span class="sxs-lookup"><span data-stu-id="102a8-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="102a8-104">Das Element SingleSignOn (Onex) gibt Single Sign-on Netzwerk Konfigurationsinformationen (SSO) an.</span><span class="sxs-lookup"><span data-stu-id="102a8-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="102a8-105">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="102a8-105">This element is optional.</span></span> <span data-ttu-id="102a8-106">Verwenden Sie das SingleSignOn-Element nicht in einem Profil, wenn es vom Netzwerk nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="102a8-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="102a8-107">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="102a8-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
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
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="102a8-108">Das **SingleSignOn** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="102a8-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="102a8-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="102a8-109">Child elements</span></span>



| <span data-ttu-id="102a8-110">Element</span><span class="sxs-lookup"><span data-stu-id="102a8-110">Element</span></span>                                                                            | <span data-ttu-id="102a8-111">type</span><span class="sxs-lookup"><span data-stu-id="102a8-111">Type</span></span>    | <span data-ttu-id="102a8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="102a8-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="102a8-113">**MaxDelay**</span><span class="sxs-lookup"><span data-stu-id="102a8-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="102a8-114">Gibt die maximale Verzögerung in Sekunden an, bevor der Single Sign-on Verbindungsversuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="102a8-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="102a8-115">**Sorte**</span><span class="sxs-lookup"><span data-stu-id="102a8-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="102a8-116">Gibt an, wann Single Sign-on ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="102a8-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="102a8-117">Wenn diese Einstellung auf festgelegt `preLogon` ist, wird Single Sign-on ausgeführt, bevor sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="102a8-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="102a8-118">Wenn diese Einstellung auf festgelegt `postLogon` ist, wird Single Sign-on sofort nach der Anmeldung des Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="102a8-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="102a8-119">**userbasedvirtuallan**</span><span class="sxs-lookup"><span data-stu-id="102a8-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="102a8-120">boolean</span><span class="sxs-lookup"><span data-stu-id="102a8-120">boolean</span></span> | <span data-ttu-id="102a8-121">Gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="102a8-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="102a8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="102a8-122">Remarks</span></span>

<span data-ttu-id="102a8-123">Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="102a8-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="102a8-124">Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="102a8-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="102a8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="102a8-125">Requirements</span></span>



| <span data-ttu-id="102a8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="102a8-126">Requirement</span></span> | <span data-ttu-id="102a8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="102a8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="102a8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="102a8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="102a8-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="102a8-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="102a8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="102a8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="102a8-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="102a8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="102a8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="102a8-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="102a8-133">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="102a8-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="102a8-134">**Onex**</span><span class="sxs-lookup"><span data-stu-id="102a8-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="102a8-135">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="102a8-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="102a8-136">**Onex**</span><span class="sxs-lookup"><span data-stu-id="102a8-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
