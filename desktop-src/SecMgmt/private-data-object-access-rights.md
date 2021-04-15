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
# <a name="private-data-object-access-rights"></a>Zugriffsrechte für private Datenobjekte

Die Zugriffs Typen dieses Objekt Typs lauten wie folgt:



| Zugriffstyp          | BESCHREIBUNG                                      |
|----------------------|--------------------------------------------------|
| geheimer \_ Abfrage \_ Wert | Dieser Zugriffstyp wird zum Abrufen eines Geheimnisses benötigt. |
| geheimer \_ \_ Wert   | Dieser Zugriffstyp ist erforderlich, um ein Geheimnis zu ändern.   |



 

## <a name="generic-access-masks"></a>Generische Zugriffs Masken

Dieser Objekttyp verfügt über die folgenden generischen Zugriffs Zuordnungen:

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Standard Zugriffs Typen:

Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht. Alle erforderlichen Zugriffs Typen werden unterstützt. Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet:

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



