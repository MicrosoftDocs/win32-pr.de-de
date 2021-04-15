---
description: Listet die Zugriffsrechte des privaten Datenobjekts auf und erläutert diese.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Zugriffsrechte für private Datenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484579"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="8b857-103">Zugriffsrechte für private Datenobjekte</span><span class="sxs-lookup"><span data-stu-id="8b857-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="8b857-104">Die Zugriffs Typen dieses Objekt Typs lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8b857-104">The access types of this object type are:</span></span>



| <span data-ttu-id="8b857-105">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8b857-105">Access type</span></span>          | <span data-ttu-id="8b857-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b857-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="8b857-107">geheimer \_ Abfrage \_ Wert</span><span class="sxs-lookup"><span data-stu-id="8b857-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="8b857-108">Dieser Zugriffstyp wird zum Abrufen eines Geheimnisses benötigt.</span><span class="sxs-lookup"><span data-stu-id="8b857-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="8b857-109">geheimer \_ \_ Wert</span><span class="sxs-lookup"><span data-stu-id="8b857-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="8b857-110">Dieser Zugriffstyp ist erforderlich, um ein Geheimnis zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8b857-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="8b857-111">Generische Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="8b857-111">Generic Access Masks</span></span>

<span data-ttu-id="8b857-112">Dieser Objekttyp verfügt über die folgenden generischen Zugriffs Zuordnungen:</span><span class="sxs-lookup"><span data-stu-id="8b857-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="8b857-113">Standard Zugriffs Typen:</span><span class="sxs-lookup"><span data-stu-id="8b857-113">Standard Access Types:</span></span>

<span data-ttu-id="8b857-114">Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht.</span><span class="sxs-lookup"><span data-stu-id="8b857-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="8b857-115">Alle erforderlichen Zugriffs Typen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b857-115">All required access types are supported.</span></span> <span data-ttu-id="8b857-116">Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet:</span><span class="sxs-lookup"><span data-stu-id="8b857-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



