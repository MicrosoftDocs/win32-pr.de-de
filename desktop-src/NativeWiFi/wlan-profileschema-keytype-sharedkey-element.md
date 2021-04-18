---
description: Gibt an, ob der gemeinsam verwendete Schlüssel ein Netzwerkschlüssel oder eine Passphrase ist.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: KeyType (sharedkey)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351711"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="4be16-103">KeyType (sharedkey)-Element</span><span class="sxs-lookup"><span data-stu-id="4be16-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="4be16-104">Das KeyType (sharedkey)-Element gibt an, ob der gemeinsam verwendete Schlüssel ein Netzwerkschlüssel oder eine Passphrase ist.</span><span class="sxs-lookup"><span data-stu-id="4be16-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="4be16-105">Das-Element wird durch das [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4be16-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be16-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4be16-106">Remarks</span></span>

<span data-ttu-id="4be16-107">Wenn das [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Element den Wert WEP hat, muss **KeyType** auf **networkkey** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4be16-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="4be16-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4be16-108">Examples</span></span>

<span data-ttu-id="4be16-109">Beispiel Profile, die das **KeyType** -Element verwenden, finden Sie unter Beispiel für [nicht-Broadcast profile](non-broadcast-profile-sample.md), [WPA-Personal Profile](wpa-personal-profile-sample.md)Sample und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4be16-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4be16-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4be16-110">Requirements</span></span>



| <span data-ttu-id="4be16-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4be16-111">Requirement</span></span> | <span data-ttu-id="4be16-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4be16-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4be16-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4be16-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4be16-114">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4be16-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4be16-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4be16-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4be16-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4be16-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="4be16-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4be16-117">Redistributable</span></span><br/>          | <span data-ttu-id="4be16-118">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="4be16-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4be16-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4be16-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="4be16-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4be16-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4be16-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="4be16-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="4be16-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4be16-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4be16-123">**sharedkey (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="4be16-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




