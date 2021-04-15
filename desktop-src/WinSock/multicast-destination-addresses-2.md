---
description: Beim Senden an eine Multicast Zieladresse erfordert das Microsoft IPv6-Protokoll normalerweise, dass für die Anwendung eine ausgehende Schnittstelle angegeben ist.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: IPv6-Multicast Zieladressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484934"
---
# <a name="ipv6-multicast-destination-addresses"></a>IPv6-Multicast Zieladressen

Beim Senden an eine Multicast Zieladresse erfordert das Microsoft IPv6-Protokoll normalerweise, dass für die Anwendung eine ausgehende Schnittstelle angegeben ist. Dies erfolgt mit der **IPv6- \_ Multicast Option \_ if** Socket oder durch Binden des Sockets an eine bestimmte Quelladresse.

Sie können auch eine Standardschnittstelle für eine bestimmte Multicast Adresse, einen gesamten Multicast Adressbereich oder alle Multicast Adressen angeben. Dies erfolgt mit einer Route, bei der das Multicast-Präfix für den Link zur gewünschten ausgehenden Schnittstelle platziert wird. In den folgenden Beispielen wird gezeigt, wie dies angegeben werden kann:

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



