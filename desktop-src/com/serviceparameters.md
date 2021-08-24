---
title: ServiceParameters
description: Gibt die Befehlszeilenparameter an, die an ein Objekt übergeben werden sollen, das zur Verwendung durch COM über den LocalService-Registrierungswert installiert wird.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- ServiceParameters-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129962"
---
# <a name="serviceparameters"></a>ServiceParameters

Gibt die Befehlszeilenparameter an, die an ein Objekt übergeben werden sollen, das zur Verwendung durch COM über den [**LocalService-Registrierungswert**](localservice.md) installiert wird.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert.** Diese Zeichenfolge wird beim Start als Befehlszeilenargument an den Dienst übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> </dl>

 

 




