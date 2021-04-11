---
title: Komplexer identityprivacyparameters-Typ
description: Enthält Informationen zur anonymen Identitäts Verwendung während der Peer-Authentifizierung.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101138"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="89d5f-103">Komplexer identityprivacyparameters-Typ</span><span class="sxs-lookup"><span data-stu-id="89d5f-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="89d5f-104">Der komplexe Typ **identityprivacyparameters** enthält Informationen zur anonymen Identitäts Verwendung während der Peer-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="89d5f-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="89d5f-105">Element</span><span class="sxs-lookup"><span data-stu-id="89d5f-105">Element</span></span>                                                                                                               | <span data-ttu-id="89d5f-106">type</span><span class="sxs-lookup"><span data-stu-id="89d5f-106">Type</span></span>    | <span data-ttu-id="89d5f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89d5f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89d5f-108">**Enableidentityprivacy**</span><span class="sxs-lookup"><span data-stu-id="89d5f-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="89d5f-109">boolean</span><span class="sxs-lookup"><span data-stu-id="89d5f-109">boolean</span></span> | <span data-ttu-id="89d5f-110">Gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="89d5f-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="89d5f-111">**AnonymousUserName**</span><span class="sxs-lookup"><span data-stu-id="89d5f-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="89d5f-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="89d5f-112">string</span></span>  | <span data-ttu-id="89d5f-113">enthält eine anonyme Identität, die anstelle der true-Identifizierung eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89d5f-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="89d5f-114">Sie wird während der ersten Phase der Peer-Authentifizierung gesendet, wenn die **Identität** als nur-Text gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="89d5f-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="89d5f-115">Die Verwendung der anonymen Identität wird vom [**enableidentityprivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) -Element bestimmt.</span><span class="sxs-lookup"><span data-stu-id="89d5f-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="89d5f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d5f-116">Remarks</span></span>

<span data-ttu-id="89d5f-117">Das identityprivacyparameters-Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="89d5f-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d5f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89d5f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d5f-119">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="89d5f-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="89d5f-120">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="89d5f-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="89d5f-121">komplexe mspeapconnectionpropertiesv2-Typen</span><span class="sxs-lookup"><span data-stu-id="89d5f-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




