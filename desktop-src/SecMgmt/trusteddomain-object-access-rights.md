---
description: Listet die Zugriffsrechte für das Objekt "Treuhänder Domäne" auf und erläutert diese.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Zugriffsrechte für das Treuhänder-Domänen Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347134"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="52086-103">Zugriffsrechte für das Treuhänder-Domänen Objekt</span><span class="sxs-lookup"><span data-stu-id="52086-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="52086-104">Der-Objekttyp " [**Treuhänder**](trusteddomain-object.md) " verfügt über die folgenden Zugriffs Typen:</span><span class="sxs-lookup"><span data-stu-id="52086-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="52086-105">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="52086-105">Access type</span></span>                  | <span data-ttu-id="52086-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52086-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="52086-107">\_ \_ Domänen \_ Name der vertrauenswürdigen Abfrage</span><span class="sxs-lookup"><span data-stu-id="52086-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="52086-108">Dieser Zugriffstyp ist erforderlich, um den Namen der vertrauenswürdigen Domäne abzufragen.</span><span class="sxs-lookup"><span data-stu-id="52086-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="52086-109">vertrauenswürdige Gruppen \_ \_ Controller</span><span class="sxs-lookup"><span data-stu-id="52086-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="52086-110">Dieser Zugriffstyp ist erforderlich, um die Liste der Controller der vertrauenswürdigen Domäne festzulegen.</span><span class="sxs-lookup"><span data-stu-id="52086-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="52086-111">POSIX der vertrauenswürdigen \_ Abfrage \_</span><span class="sxs-lookup"><span data-stu-id="52086-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="52086-112">Dieser Zugriffstyp ist erforderlich, um den POSIX-ID-Offset einer vertrauenswürdigen Domäne abzurufen.</span><span class="sxs-lookup"><span data-stu-id="52086-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="52086-113">\_festgelegte \_ POSIX-Menge</span><span class="sxs-lookup"><span data-stu-id="52086-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="52086-114">Dieser Zugriffstyp ist erforderlich, um den POSIX-ID-Offset einer vertrauenswürdigen Domäne festzulegen.</span><span class="sxs-lookup"><span data-stu-id="52086-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="52086-115">Generische Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="52086-115">Generic Access Masks</span></span>

<span data-ttu-id="52086-116">Dieser Objekttyp verfügt über die folgenden generischen Zugriffs Zuordnungen:</span><span class="sxs-lookup"><span data-stu-id="52086-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="52086-117">Standard Zugriffs Typen</span><span class="sxs-lookup"><span data-stu-id="52086-117">Standard Access Types</span></span>

<span data-ttu-id="52086-118">Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht.</span><span class="sxs-lookup"><span data-stu-id="52086-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="52086-119">Alle erforderlichen Zugriffs Typen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52086-119">All required access types are supported.</span></span> <span data-ttu-id="52086-120">Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet:</span><span class="sxs-lookup"><span data-stu-id="52086-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



