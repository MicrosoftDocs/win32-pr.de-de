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
# <a name="endpoints"></a><span data-ttu-id="7e288-104">Endpunkte</span><span class="sxs-lookup"><span data-stu-id="7e288-104">Endpoints</span></span>

<span data-ttu-id="7e288-105">Konfiguriert eine COM-Anwendung so, dass eine angegebene TCP-Portnummer für die DCOM-Kommunikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e288-105">Configures a COM application to use a specified TCP port number for DCOM communications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7e288-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="7e288-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a><span data-ttu-id="7e288-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e288-107">Remarks</span></span>

<span data-ttu-id="7e288-108">Dies ist ein **reg \_ \_ MultiSZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="7e288-108">This is a **REG\_MULTI\_SZ** value.</span></span>

<span data-ttu-id="7e288-109">Der *Portwert* ist eine Zahl zwischen 1024 und 65535, die die TCP-Portnummer angibt, die von der com-Anwendung für die DCOM-Kommunikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e288-109">The *port* value is a number between 1024 and 65535 that specifies the TCP port number that your COM application will use for DCOM communications.</span></span> <span data-ttu-id="7e288-110">Wenn Sie diesen Registrierungsschlüssel nicht angeben, werden die Portnummern für die DCOM-Kommunikation dynamisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7e288-110">If you do not specify this registry key, port numbers for DCOM communications are dynamically assigned.</span></span> <span data-ttu-id="7e288-111">In den meisten Szenarien empfiehlt es sich, diesen Registrierungsschlüssel nicht definiert zu lassen und DCOM das dynamische Zuweisen von Portnummern zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="7e288-111">In most scenarios, you might prefer to leave this registry key undefined and allow DCOM to dynamically assign port numbers.</span></span>

 

 




