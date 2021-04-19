---
description: Enthält Informationen zu gemeinsam genutzten Schlüsseln.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: sharedkey-Element (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363527"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="19592-103">sharedkey-Element (Security)</span><span class="sxs-lookup"><span data-stu-id="19592-103">sharedKey (security) Element</span></span>

<span data-ttu-id="19592-104">Das sharedkey-Element (Security) enthält Informationen zu gemeinsam genutzten Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="19592-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="19592-105">Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="19592-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="19592-106">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="19592-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="19592-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19592-107">Child elements</span></span>



| <span data-ttu-id="19592-108">Element</span><span class="sxs-lookup"><span data-stu-id="19592-108">Element</span></span>                                                                 | <span data-ttu-id="19592-109">type</span><span class="sxs-lookup"><span data-stu-id="19592-109">Type</span></span>                                                              | <span data-ttu-id="19592-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19592-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19592-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="19592-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="19592-112">string</span><span class="sxs-lookup"><span data-stu-id="19592-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="19592-113">Enthält den Netzwerkschlüssel oder die Passphrase.</span><span class="sxs-lookup"><span data-stu-id="19592-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="19592-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="19592-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="19592-115">Der Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="19592-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="19592-116">**protected**</span><span class="sxs-lookup"><span data-stu-id="19592-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="19592-117">boolean</span><span class="sxs-lookup"><span data-stu-id="19592-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="19592-118">Gibt an, ob der Schlüssel verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="19592-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="19592-119">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert false aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19592-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="19592-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19592-120">Remarks</span></span>

<span data-ttu-id="19592-121">Für Windows Vista und Windows Server 2008 werden die dem **sharedkey** -Element zugeordneten Daten vor dem Speichern im Profil Speicher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="19592-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="19592-122">Für Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2 werden die Daten nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="19592-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="19592-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19592-123">Examples</span></span>

<span data-ttu-id="19592-124">Beispiel Profile, die das **sharedkey** -Element verwenden, finden Sie unter Beispiel für [nicht-Broadcast profile](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md)und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="19592-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19592-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19592-125">Requirements</span></span>



| <span data-ttu-id="19592-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19592-126">Requirement</span></span> | <span data-ttu-id="19592-127">Wert</span><span class="sxs-lookup"><span data-stu-id="19592-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19592-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19592-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19592-129">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19592-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19592-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19592-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19592-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19592-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="19592-132">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="19592-132">Redistributable</span></span><br/>          | <span data-ttu-id="19592-133">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="19592-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="19592-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19592-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="19592-135">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="19592-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="19592-136">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="19592-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="19592-137">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="19592-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="19592-138">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="19592-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
