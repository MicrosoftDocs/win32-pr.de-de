---
title: Komplexer Typ "kredentialssourceparameters"
description: Definiert das Element, das zum Angeben der Quelle des Zertifikats erforderlich ist, das mit einer EAP-TLS-Authentifizierung verwendet werden soll.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- Der komplexe Typ "fidentialssourceparameters" EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104870"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="de857-104">Komplexer Typ "kredentialssourceparameters"</span><span class="sxs-lookup"><span data-stu-id="de857-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="de857-105">Der komplexe Typ " **fordentialssourceparameters** " definiert das Element, das zum Angeben der Quelle des Zertifikats erforderlich ist, das mit einer EAP-TLS-Authentifizierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="de857-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="de857-106">Zwischen dem [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) -Element oder dem [**certifikatestore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) -Element kann eine Auswahl getroffen werden.</span><span class="sxs-lookup"><span data-stu-id="de857-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="de857-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de857-107">Child elements</span></span>



| <span data-ttu-id="de857-108">Element</span><span class="sxs-lookup"><span data-stu-id="de857-108">Element</span></span>                                                                                                             | <span data-ttu-id="de857-109">type</span><span class="sxs-lookup"><span data-stu-id="de857-109">Type</span></span>                                                                                  | <span data-ttu-id="de857-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de857-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de857-111">**CertificateStore**</span><span class="sxs-lookup"><span data-stu-id="de857-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="de857-112">**Certselection**</span><span class="sxs-lookup"><span data-stu-id="de857-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="de857-113">Gibt an, dass EAP-TLS das Zertifikat aus dem eigenen Speicher des Benutzers oder dem Computer lesen soll, der authentifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="de857-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="de857-114">**Smartcard**</span><span class="sxs-lookup"><span data-stu-id="de857-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="de857-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="de857-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="de857-116">Gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll.</span><span class="sxs-lookup"><span data-stu-id="de857-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="de857-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de857-117">Remarks</span></span>

<span data-ttu-id="de857-118">Die [**certifikatestore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) -und [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) -Elemente können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de857-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="de857-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de857-119">Requirements</span></span>



| <span data-ttu-id="de857-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de857-120">Requirement</span></span> | <span data-ttu-id="de857-121">Wert</span><span class="sxs-lookup"><span data-stu-id="de857-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de857-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de857-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de857-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de857-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de857-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de857-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de857-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de857-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de857-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de857-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de857-127">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="de857-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="de857-128">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="de857-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="de857-129">komplexe eaptlsconnectionpropertiesv1-Schema Typen</span><span class="sxs-lookup"><span data-stu-id="de857-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





