---
description: Es gibt eine Einschränkung im Code, der gekapselte (getunnelte) Pakete empfängt und diese an eine bestimmte Schnittstelle demultiplext.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Getunnelte IPv6-Weiterleitungspakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42138c746ea9d0ec8ea61bc3801b84a97a6bdd4c6fb6de0871e6b74447fdf28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132433"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Getunnelte IPv6-Weiterleitungspakete

Es gibt eine Einschränkung im Code, der gekapselte (getunnelte) Pakete empfängt und diese an eine bestimmte Schnittstelle demultiplext. Wenn Sie getunnelte Pakete weiterleiten möchten, die über einen konfigurierten Tunnel empfangen wurden, müssen Sie die Weiterleitung für alle 6-über-4-Schnittstellen sowie die Schnittstelle \# 2 aktivieren. Das Aktivieren der Weiterleitung auf Schnittstelle \# 2 funktioniert nicht. In der Regel würden Sie beim Konfigurieren eines Routers die Weiterleitung für alle Schnittstellen außer Loopback aktivieren.

 

 



