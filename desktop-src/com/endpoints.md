---
title: Endpunkte
description: Konfiguriert eine COM-Anwendung so, dass eine angegebene TCP-Portnummer für die DCOM-Kommunikation verwendet wird.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Registrierungs Wert für Endpunkte (com)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388152"
---
# <a name="endpoints"></a>Endpunkte

Konfiguriert eine COM-Anwendung so, dass eine angegebene TCP-Portnummer für die DCOM-Kommunikation verwendet wird.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ \_ MultiSZ** -Wert.

Der *Portwert* ist eine Zahl zwischen 1024 und 65535, die die TCP-Portnummer angibt, die von der com-Anwendung für die DCOM-Kommunikation verwendet wird. Wenn Sie diesen Registrierungsschlüssel nicht angeben, werden die Portnummern für die DCOM-Kommunikation dynamisch zugewiesen. In den meisten Szenarien empfiehlt es sich, diesen Registrierungsschlüssel nicht definiert zu lassen und DCOM das dynamische Zuweisen von Portnummern zuzulassen.

 

 




