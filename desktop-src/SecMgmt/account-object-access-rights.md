---
description: Der Kontoobjekt-Zugriffsberechtigungstyp weist die folgenden Zugriffstypen auf.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Zugriffsrechte für Kontoobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1251eecfd32bc574307cbc4f0f1327e4f96eb7fa7051d1dd638beb59e7ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895107"
---
# <a name="account-object-access-rights"></a>Zugriffsrechte für Kontoobjekte

Der Kontoobjekt-Zugriffsberechtigungstyp weist die folgenden Zugriffstypen auf.



| Zugriffstyp                     | BESCHREIBUNG                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_KONTOANSICHT                   | Dieser Zugriffstyp ist erforderlich, um die Kontoinformationen zu lesen. Dies schließt die dem Konto zugewiesenen [*Berechtigungen,*](/windows/desktop/SecGloss/p-gly) zugewiesene Arbeitsspeicherkontingente und alle gewährten speziellen Zugriffstypen ein. |
| \_ \_ KONTOANPASSUNGSBERECHTIGUNGEN     | Dieser Zugriffstyp ist erforderlich, um einem Konto Berechtigungen zuzuweisen oder Berechtigungen daraus zu entfernen.                                                                                                                                                            |
| KONTINGENTE ANPASSEN DES \_ \_ KONTOS         | Dieser Zugriffstyp ist erforderlich, um die einem Konto zugewiesenen Systemkontingente zu ändern.                                                                                                                                                                      |
| KONTO \_ ANPASSEN \_ DES \_ SYSTEMZUGRIFFS | Dieser Zugriffstyp ist erforderlich, um die Systemzugriffsflags für das Konto zu aktualisieren.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Generische Zugriffsmasken

Das [**Account-Objekt**](account-object.md) veröffentlicht die folgenden Zuordnungen von generischen Zugriffstypen zu bestimmten Zugriffstypen.

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Standardzugriffstypen

Dieses Objekt unterstützt den (optionalen) SYNCHRONIZE-Standardzugriffstyp nicht. Alle erforderlichen Zugriffstypen werden unterstützt. Die Maske aller unterstützten Zugriffstypen für diesen Objekttyp lautet wie folgt.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
