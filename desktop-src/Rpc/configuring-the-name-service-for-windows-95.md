---
title: Konfigurieren des Namens Dienstanbieter für Windows 95
description: Windows 95 verwendet nicht den Microsoft-Locator.
ms.assetid: 0903681c-9cbf-4c5c-8637-be7f6501cd14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910a2cdc2d7a0543e07591ff37523169c311a3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712006"
---
# <a name="configuring-the-name-service-for-windows-95"></a>Konfigurieren des Namens Dienstanbieter für Windows 95

Windows 95 verwendet nicht den Microsoft-Locator. Damit ein Namensdienst in einer Windows 95-Anwendung verwendet werden kann, muss auf dem Computer mit Windows 95 Folgendes verwendet werden:

-   Sie müssen Teil einer Arbeitsgruppe oder Domäne sein, die einen Computer mit Windows 2000 oder Windows NT enthält, der als Proxy Namen Dienstanbieter fungiert.
-   Sie müssen mit einem Host Computer verbunden sein, auf dem der NSI-Daemon (nsid) ausgeführt wird, der als Gateway für den DCE-Zell Verzeichnisdienst der Digital Equipment Corporation fungiert.

 

 




