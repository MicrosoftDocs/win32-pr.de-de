---
title: Service Parameters
description: Gibt die Befehlszeilenparameter an, die an ein Objekt zu übertragen sind, das zur Verwendung durch com über den Registrierungs Wert LocalService installiert wird.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Registrierungs Wert von Service Parameters com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310123"
---
# <a name="serviceparameters"></a>Service Parameters

Gibt die Befehlszeilenparameter an, die an ein Objekt zu übertragen sind, das zur Verwendung durch com über den Registrierungs Wert [**LocalService**](localservice.md) installiert wird.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert. Diese Zeichenfolge wird beim Start als Befehlszeilenargument an den Dienst übermittelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> </dl>

 

 




