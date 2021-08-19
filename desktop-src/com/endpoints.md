---
title: Endpunkte
description: Konfiguriert eine COM-Anwendung für die Verwendung einer angegebenen TCP-Portnummer für die DCOM-Kommunikation.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Endpunktregistrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ee2444be55aaf32c028792100e3e6f0ed6989509b7c0af02c5d83bd739fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048318"
---
# <a name="endpoints"></a>Endpunkte

Konfiguriert eine COM-Anwendung für die Verwendung einer angegebenen TCP-Portnummer für die DCOM-Kommunikation.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ MULTI \_ SZ-Wert.**

Der *Portwert* ist eine Zahl zwischen 1024 und 65535, die die TCP-Portnummer angibt, die Ihre COM-Anwendung für die DCOM-Kommunikation verwendet. Wenn Sie diesen Registrierungsschlüssel nicht angeben, werden Portnummern für die DCOM-Kommunikation dynamisch zugewiesen. In den meisten Szenarien sollten Sie diesen Registrierungsschlüssel undefiniert lassen und DCOM erlauben, Portnummern dynamisch zu zuweisen.

 

 




