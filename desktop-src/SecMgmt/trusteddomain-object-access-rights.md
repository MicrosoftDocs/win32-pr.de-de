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
# <a name="trusteddomain-object-access-rights"></a>Zugriffsrechte für das Treuhänder-Domänen Objekt

Der-Objekttyp " [**Treuhänder**](trusteddomain-object.md) " verfügt über die folgenden Zugriffs Typen:



| Zugriffstyp                  | BESCHREIBUNG                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| \_ \_ Domänen \_ Name der vertrauenswürdigen Abfrage | Dieser Zugriffstyp ist erforderlich, um den Namen der vertrauenswürdigen Domäne abzufragen.              |
| vertrauenswürdige Gruppen \_ \_ Controller    | Dieser Zugriffstyp ist erforderlich, um die Liste der Controller der vertrauenswürdigen Domäne festzulegen. |
| POSIX der vertrauenswürdigen \_ Abfrage \_        | Dieser Zugriffstyp ist erforderlich, um den POSIX-ID-Offset einer vertrauenswürdigen Domäne abzurufen.  |
| \_festgelegte \_ POSIX-Menge          | Dieser Zugriffstyp ist erforderlich, um den POSIX-ID-Offset einer vertrauenswürdigen Domäne festzulegen.       |



 

## <a name="generic-access-masks"></a>Generische Zugriffs Masken

Dieser Objekttyp verfügt über die folgenden generischen Zugriffs Zuordnungen:

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Standard Zugriffs Typen

Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht. Alle erforderlichen Zugriffs Typen werden unterstützt. Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



