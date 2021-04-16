---
description: Der Typ der Konto Objekt-Zugriffsrechte weist die folgenden Zugriffs Typen auf.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Zugriffsrechte für Konto Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529648"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="f4c50-103">Zugriffsrechte für Konto Objekte</span><span class="sxs-lookup"><span data-stu-id="f4c50-103">Account Object Access Rights</span></span>

<span data-ttu-id="f4c50-104">Der Typ der Konto Objekt-Zugriffsrechte weist die folgenden Zugriffs Typen auf.</span><span class="sxs-lookup"><span data-stu-id="f4c50-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="f4c50-105">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f4c50-105">Access type</span></span>                     | <span data-ttu-id="f4c50-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4c50-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c50-107">Konto \_ Ansicht</span><span class="sxs-lookup"><span data-stu-id="f4c50-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="f4c50-108">Dieser Zugriffstyp ist erforderlich, um die Kontoinformationen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f4c50-108">This access type is required to read the account information.</span></span> <span data-ttu-id="f4c50-109">Dies schließt die dem Konto zugewiesenen [*Berechtigungen*](/windows/desktop/SecGloss/p-gly) , zugewiesene Arbeitsspeicher Kontingente und alle gewährten speziellen Zugriffs Typen ein.</span><span class="sxs-lookup"><span data-stu-id="f4c50-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="f4c50-110">Konto \_ Anpassungs \_ Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="f4c50-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="f4c50-111">Dieser Zugriffstyp ist erforderlich, um Berechtigungen für ein Konto zuzuweisen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f4c50-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="f4c50-112">Konto \_ Anpassungs \_ Kontingente</span><span class="sxs-lookup"><span data-stu-id="f4c50-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="f4c50-113">Dieser Zugriffstyp ist erforderlich, um die einem Konto zugewiesenen System Kontingente zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f4c50-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="f4c50-114">Konto \_ Anpassung des \_ System \_ Zugriffs</span><span class="sxs-lookup"><span data-stu-id="f4c50-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="f4c50-115">Dieser Zugriffstyp ist erforderlich, um die systemzugriffsflags für das Konto zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f4c50-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="f4c50-116">Generische Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="f4c50-116">Generic Access Masks</span></span>

<span data-ttu-id="f4c50-117">Das [**Account**](account-object.md) -Objekt veröffentlicht die folgenden Zuordnungen von generischen Zugriffs Typen auf bestimmte Zugriffs Typen.</span><span class="sxs-lookup"><span data-stu-id="f4c50-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="f4c50-118">Standard Zugriffs Typen</span><span class="sxs-lookup"><span data-stu-id="f4c50-118">Standard Access Types</span></span>

<span data-ttu-id="f4c50-119">Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht.</span><span class="sxs-lookup"><span data-stu-id="f4c50-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="f4c50-120">Alle erforderlichen Zugriffs Typen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4c50-120">All required access types are supported.</span></span> <span data-ttu-id="f4c50-121">Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="f4c50-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
