---
description: Listet die Zugriffsrechte des TrustedDomain-Objekts auf und erläutert sie.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Zugriffsrechte für TrustedDomain-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efeaf621cc3727cb936e69806bbcf89dabe5d41eb39b38dce3f9f23a0200dcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893008"
---
# <a name="trusteddomain-object-access-rights"></a>Zugriffsrechte für TrustedDomain-Objekte

Der [**TrustedDomain-Objekttyp**](trusteddomain-object.md) verfügt über die folgenden Zugriffstypen:



| Zugriffstyp                  | Beschreibung                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| DOMÄNENNAME \_ DER \_ VERTRAUENSWÜRDIGEN \_ ABFRAGE | Dieser Zugriffstyp ist erforderlich, um den Namen der vertrauenswürdigen Domäne abfragen zu können.              |
| \_VERTRAUENSWÜRDIGE \_ SET-CONTROLLER    | Dieser Zugriffstyp ist erforderlich, um die Liste der Controller der vertrauenswürdigen Domäne festlegen zu können. |
| TRUSTED \_ QUERY \_ POSIX        | Dieser Zugriffstyp ist erforderlich, um den Posix-ID-Offset einer vertrauenswürdigen Domäne abzurufen.  |
| TRUSTED \_ SET \_ POSIX          | Dieser Zugriffstyp ist erforderlich, um den Posix-ID-Offset einer vertrauenswürdigen Domäne festlegen zu können.       |



 

## <a name="generic-access-masks"></a>Generische Zugriffsmasken

Dieser Objekttyp verfügt über die folgenden generischen Zugriffszuordnungen:

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Standardzugriffstypen

Dieses Objekt unterstützt den (optionalen) SYNCHRONIZE-Standardzugriffstyp nicht. Alle erforderlichen Zugriffstypen werden unterstützt. Die Maske aller unterstützten Zugriffstypen für diesen Objekttyp ist:

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



