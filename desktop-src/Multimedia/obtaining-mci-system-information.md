---
title: Abrufen von MCI-System Informationen
description: Abrufen von MCI-System Informationen
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947618"
---
# <a name="obtaining-mci-system-information"></a>Abrufen von MCI-System Informationen

Der [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md))-Befehl ruft Systeminformationen zu MCI-Geräten ab. MCI verarbeitet diesen Befehl, ohne ihn an ein beliebiges MCI-Gerät weiterleiten zu müssen. Für die befehlsnachrichten Schnittstelle gibt MCI die Systeminformationen in der [**MCI- \_ sysinfo \_**](mci-sysinfo-parms.md) -Struktur des Parametern zurück.

Sie können den **sysinfo** (MCI \_ sysinfo)-Befehl verwenden, um Informationen wie die Anzahl der MCI-Geräte auf einem System, die Anzahl der MCI-Geräte eines bestimmten Typs, die Anzahl der geöffneten MCI-Geräte und die Namen der Geräte abzurufen. Dieser Befehl wird häufig mehrmals aufgerufen, um ein bestimmtes Informationselement abzurufen. Beispielsweise können Sie die Anzahl der Geräte eines bestimmten Typs im ersten-Befehl Abrufen und dann die Namen der Geräte in der nächsten Aufzählung.

 

 




