---
title: Komplexer baseeapmethoduseranmeldeinyp
description: Erfahren Sie mehr über den komplexen Basistyp baseeapmethoduseranmeldeinformationen. Dieser Typ ist ein Platzhalter Element für Methoden Anmelde Informationsdaten.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Der komplexe Typ "baseeapmethoduseranmeldeinformationen" EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730177"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="34bd8-105">Komplexer baseeapmethoduseranmeldeinyp</span><span class="sxs-lookup"><span data-stu-id="34bd8-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="34bd8-106">Der komplexe **Basistyp baseeapmethodusercredenist** ein Platzhalter Element für Anmelde Informationsdaten der Methode.</span><span class="sxs-lookup"><span data-stu-id="34bd8-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="34bd8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34bd8-107">Remarks</span></span>

<span data-ttu-id="34bd8-108">Die EAP-Methode führt eine Schema Validierung für den Inhalt von **baseeapmethoduseranmelde** Informationen durch.</span><span class="sxs-lookup"><span data-stu-id="34bd8-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="34bd8-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34bd8-109">Requirements</span></span>



| <span data-ttu-id="34bd8-110">Role</span><span class="sxs-lookup"><span data-stu-id="34bd8-110">Role</span></span> | <span data-ttu-id="34bd8-111">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="34bd8-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="34bd8-112">Client</span><span class="sxs-lookup"><span data-stu-id="34bd8-112">Client</span></span><br/> | <span data-ttu-id="34bd8-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34bd8-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="34bd8-114">Server</span><span class="sxs-lookup"><span data-stu-id="34bd8-114">Server</span></span><br/> | <span data-ttu-id="34bd8-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34bd8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34bd8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34bd8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34bd8-117">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="34bd8-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="34bd8-118">baseeapmethoduseranmeldeinformationen-Schema</span><span class="sxs-lookup"><span data-stu-id="34bd8-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





