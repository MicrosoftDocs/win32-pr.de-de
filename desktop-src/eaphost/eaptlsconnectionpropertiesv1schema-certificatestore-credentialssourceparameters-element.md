---
title: Certifikatestore ("kredentialssourceparameters")-Element
description: Gibt an, dass EAP-TLS das Zertifikat aus dem eigenen Speicher des Benutzers oder dem Computer lesen soll, der authentifiziert wird.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Certifikatestore-Element EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518332"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="3a37f-104">Certifikatestore ("kredentialssourceparameters")-Element</span><span class="sxs-lookup"><span data-stu-id="3a37f-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="3a37f-105">Das **CertificateStore ("kredentialssourceparameters")** -Element gibt an, dass EAP-TLS das Zertifikat aus dem eigenen Speicher des Benutzers oder dem Computer lesen soll, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3a37f-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="3a37f-106">Das **certifikatestore** -Element wird durch den komplexen Typ " [**fordentialssourceparameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="3a37f-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a37f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a37f-107">Remarks</span></span>

<span data-ttu-id="3a37f-108">Die **certifikatestore** -und [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) -Elemente können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a37f-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a37f-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a37f-109">Requirements</span></span>



| <span data-ttu-id="3a37f-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a37f-110">Requirement</span></span> | <span data-ttu-id="3a37f-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3a37f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a37f-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a37f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3a37f-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a37f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a37f-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a37f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3a37f-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a37f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a37f-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a37f-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a37f-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="3a37f-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3a37f-118">**"Kredentialssourceparameters"**</span><span class="sxs-lookup"><span data-stu-id="3a37f-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="3a37f-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="3a37f-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3a37f-120">**"Kredentialssource" (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="3a37f-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="3a37f-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3a37f-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3a37f-122">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="3a37f-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3a37f-123">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="3a37f-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3a37f-124">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="3a37f-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





