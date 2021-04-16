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
# <a name="account-object-access-rights"></a>Zugriffsrechte für Konto Objekte

Der Typ der Konto Objekt-Zugriffsrechte weist die folgenden Zugriffs Typen auf.



| Zugriffstyp                     | BESCHREIBUNG                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konto \_ Ansicht                   | Dieser Zugriffstyp ist erforderlich, um die Kontoinformationen zu lesen. Dies schließt die dem Konto zugewiesenen [*Berechtigungen*](/windows/desktop/SecGloss/p-gly) , zugewiesene Arbeitsspeicher Kontingente und alle gewährten speziellen Zugriffs Typen ein. |
| Konto \_ Anpassungs \_ Berechtigungen     | Dieser Zugriffstyp ist erforderlich, um Berechtigungen für ein Konto zuzuweisen oder zu entfernen.                                                                                                                                                            |
| Konto \_ Anpassungs \_ Kontingente         | Dieser Zugriffstyp ist erforderlich, um die einem Konto zugewiesenen System Kontingente zu ändern.                                                                                                                                                                      |
| Konto \_ Anpassung des \_ System \_ Zugriffs | Dieser Zugriffstyp ist erforderlich, um die systemzugriffsflags für das Konto zu aktualisieren.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Generische Zugriffs Masken

Das [**Account**](account-object.md) -Objekt veröffentlicht die folgenden Zuordnungen von generischen Zugriffs Typen auf bestimmte Zugriffs Typen.

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Standard Zugriffs Typen

Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht. Alle erforderlichen Zugriffs Typen werden unterstützt. Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet wie folgt.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
