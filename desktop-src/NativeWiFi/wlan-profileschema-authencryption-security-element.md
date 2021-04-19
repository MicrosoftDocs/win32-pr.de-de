---
description: Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: authencryption (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345810"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="975ca-103">authencryption (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="975ca-103">authEncryption (security) Element</span></span>

<span data-ttu-id="975ca-104">Das authencryption (Security)-Element gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="975ca-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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

<span data-ttu-id="975ca-105">Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="975ca-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="975ca-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="975ca-106">Child elements</span></span>



| <span data-ttu-id="975ca-107">Element</span><span class="sxs-lookup"><span data-stu-id="975ca-107">Element</span></span>                                                                            | <span data-ttu-id="975ca-108">type</span><span class="sxs-lookup"><span data-stu-id="975ca-108">Type</span></span>                                                              | <span data-ttu-id="975ca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="975ca-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="975ca-110">**Genehmigung**</span><span class="sxs-lookup"><span data-stu-id="975ca-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="975ca-111">Gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="975ca-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="975ca-112">**Verschlüsselungs**</span><span class="sxs-lookup"><span data-stu-id="975ca-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="975ca-113">Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="975ca-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="975ca-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="975ca-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="975ca-115">boolean</span><span class="sxs-lookup"><span data-stu-id="975ca-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="975ca-116">Gibt an, ob 802.1 x verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="975ca-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="975ca-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="975ca-117">Remarks</span></span>

<span data-ttu-id="975ca-118">Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) **authencryption** -Elements eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="975ca-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="975ca-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="975ca-119">Examples</span></span>

<span data-ttu-id="975ca-120">Beispiel Profile, die das **authencryption** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="975ca-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="975ca-121">Ein Beispiel Profil, das das-Element in der-Datei verwendet, finden Sie unter Beispiel für das [**PPS**](wlan-profileschema-fipsmode-authencryption-element.md) - [Profil](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="975ca-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="975ca-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="975ca-122">Requirements</span></span>



| <span data-ttu-id="975ca-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="975ca-123">Requirement</span></span> | <span data-ttu-id="975ca-124">Wert</span><span class="sxs-lookup"><span data-stu-id="975ca-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="975ca-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="975ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="975ca-126">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="975ca-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="975ca-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="975ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="975ca-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="975ca-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="975ca-129">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="975ca-129">Redistributable</span></span><br/>          | <span data-ttu-id="975ca-130">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="975ca-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="975ca-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="975ca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975ca-132">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="975ca-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="975ca-133">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="975ca-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="975ca-134">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="975ca-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="975ca-135">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="975ca-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="975ca-136">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="975ca-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
