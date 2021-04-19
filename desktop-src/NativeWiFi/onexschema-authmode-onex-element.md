---
description: Gibt den Typ der für die Authentifizierung verwendeten Anmelde Informationen an.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: authmode-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356708"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="11f85-103">authmode-Element (Onex)</span><span class="sxs-lookup"><span data-stu-id="11f85-103">authMode (OneX) Element</span></span>

<span data-ttu-id="11f85-104">Das authmode (Onex)-Element gibt den Typ der Anmelde Informationen an, die für die Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11f85-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="11f85-105">In der folgenden Tabelle sind die möglichen Werte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="11f85-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="11f85-106">Wert</span><span class="sxs-lookup"><span data-stu-id="11f85-106">Value</span></span>         | <span data-ttu-id="11f85-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11f85-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f85-108">machineoruser</span><span class="sxs-lookup"><span data-stu-id="11f85-108">machineOrUser</span></span> | <span data-ttu-id="11f85-109">Verwenden Sie Computer-oder Benutzer Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="11f85-109">Use machine or user credentials.</span></span> <span data-ttu-id="11f85-110">Wenn ein Benutzer angemeldet ist, werden die Anmelde Informationen des Benutzers zur Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="11f85-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="11f85-111">Wenn kein Benutzer angemeldet ist, werden Computer Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="11f85-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="11f85-112">Computer</span><span class="sxs-lookup"><span data-stu-id="11f85-112">machine</span></span>       | <span data-ttu-id="11f85-113">Verwenden Sie nur Computer Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="11f85-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="11f85-114">user</span><span class="sxs-lookup"><span data-stu-id="11f85-114">user</span></span>          | <span data-ttu-id="11f85-115">Nur Benutzer Anmelde Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="11f85-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="11f85-116">guest</span><span class="sxs-lookup"><span data-stu-id="11f85-116">guest</span></span>         | <span data-ttu-id="11f85-117">Nur Gast Anmelde Informationen (leer) verwenden.</span><span class="sxs-lookup"><span data-stu-id="11f85-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="11f85-118">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="11f85-118">This element is optional.</span></span> <span data-ttu-id="11f85-119">Wenn authmode nicht in einem Profil angegeben ist, wird der Wert `machineOrUser` verwendet.</span><span class="sxs-lookup"><span data-stu-id="11f85-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="11f85-120">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="11f85-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="11f85-121">Das **authmode** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="11f85-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="11f85-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11f85-122">Remarks</span></span>

<span data-ttu-id="11f85-123">Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="11f85-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="11f85-124">Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="11f85-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="11f85-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11f85-125">Requirements</span></span>



| <span data-ttu-id="11f85-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11f85-126">Requirement</span></span> | <span data-ttu-id="11f85-127">Wert</span><span class="sxs-lookup"><span data-stu-id="11f85-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11f85-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11f85-128">Minimum supported client</span></span><br/> | <span data-ttu-id="11f85-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11f85-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11f85-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11f85-130">Minimum supported server</span></span><br/> | <span data-ttu-id="11f85-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11f85-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11f85-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11f85-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="11f85-133">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="11f85-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="11f85-134">**Onex**</span><span class="sxs-lookup"><span data-stu-id="11f85-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="11f85-135">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="11f85-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="11f85-136">**Onex**</span><span class="sxs-lookup"><span data-stu-id="11f85-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
