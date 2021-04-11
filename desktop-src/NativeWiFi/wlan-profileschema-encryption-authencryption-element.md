---
description: Gibt den Typ der Datenverschlüsselung an, die zum Herstellen einer Verbindung mit einem drahtlosen LAN verwendet werden soll.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Encryption-Element (authencryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129729"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="02789-103">Encryption-Element (authencryption)</span><span class="sxs-lookup"><span data-stu-id="02789-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="02789-104">Das Encryption (authencryption)-Element gibt den Typ der Datenverschlüsselung an, die zum Herstellen einer Verbindung mit einem drahtlosen LAN verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="02789-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="02789-105">Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="02789-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="02789-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02789-106">Remarks</span></span>

<span data-ttu-id="02789-107">Wenn das **Verschlüsselungs** Element den Wert WEP hat, muss [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) auf **networkkey** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="02789-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="02789-108">Die AES-Verschlüsselungsmethode ist gemäß den Spezifikationen [802.1 x](https://ieeexplore.ieee.org/document/1438730) und [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) angegeben.</span><span class="sxs-lookup"><span data-stu-id="02789-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="02789-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02789-109">Examples</span></span>

<span data-ttu-id="02789-110">Beispiel Profile, die das- **Verschlüsselungs** Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="02789-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02789-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02789-111">Requirements</span></span>



| <span data-ttu-id="02789-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02789-112">Requirement</span></span> | <span data-ttu-id="02789-113">Wert</span><span class="sxs-lookup"><span data-stu-id="02789-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="02789-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02789-114">Minimum supported client</span></span><br/> | <span data-ttu-id="02789-115">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02789-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02789-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02789-116">Minimum supported server</span></span><br/> | <span data-ttu-id="02789-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02789-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="02789-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="02789-118">Redistributable</span></span><br/>          | <span data-ttu-id="02789-119">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="02789-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="02789-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02789-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="02789-121">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="02789-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="02789-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="02789-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="02789-123">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="02789-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="02789-124">**authencryption (Sicherheit)**</span><span class="sxs-lookup"><span data-stu-id="02789-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




