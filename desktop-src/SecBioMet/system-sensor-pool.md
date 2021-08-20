---
title: Systemsensorpool
description: Eine Sammlung von biometrischen Einheiten, die den Zugriff auf Windows Authentifizierungsdienste ermöglichen. Dieser Pool wird von Winlogon, UAC und jedem anderen Client verwendet, der eine SID einer bestimmten biometrischen Vorlage zustimmt.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c73a187c81812355d574b6c4fb867aad8f832c504f7ec79289879565cf73bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911613"
---
# <a name="system-sensor-pool"></a>Systemsensorpool

Der Systemsensorpool ist eine Sammlung von biometrischen Einheiten, die den Zugriff auf Windows Authentifizierungsdienste ermöglichen. Dieser Pool wird von Winlogon, UAC und jedem anderen Client verwendet, der eine SID einer bestimmten biometrischen Vorlage zustimmt. Biometrische Einheiten im Systempool:

-   Kann von mehreren Clientanwendungen gemeinsam genutzt werden.
-   Senden Sie Ereignishinweise, die durch den Abschluss biometrischer Vorgänge generiert werden, nur an die Anwendung, die den aktuellen Fensterfokus besitzt.
-   Verwenden Sie Konto-SIDs, um die Vorlagenidentitäten darzustellen. Alle Vorlagen, die einem einzelnen Benutzerkonto zugeordnet sind, werden mit der SID gekennzeichnet, die diesem Konto zugewiesen ist.
-   Hängen Sie vom vertrauenswürdigen Vorlagenspeicher ab, der vom Windows Biometric Service bereitgestellt wird.

Eine biometrische Einheit kann in den Systempool aufgenommen werden, wenn dies der Folgende ist:

-   Konfiguriert für den Betrieb im Basic-Modus und fungiert nur als biometrisches Erfassungsgerät.
-   Konfiguriert für den Betrieb im erweiterten Modus, verfügt aber über keinen integrierten Vorlagenspeicher. Das heißt, er muss den von Microsoft bereitgestellten Speicheradapter und Vorlagenspeicher verwenden.
-   Konfiguriert für den Betrieb im erweiterten Modus, enthält integrierten Vorlagenspeicher und kann die erforderlichen Hashes generieren.

Wenn ein neues Sensorgerät angeschlossen ist, erstellt der Windows Biometric Service eine biometrische Einheit dafür und versucht, diese Einheit für die Verwendung durch den Systemsensorpool zu konfigurieren. Wenn die Konfiguration nicht erfolgreich ist, wird die biometrische Einheit im nicht zugewiesenen Sensorpool platziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Privater Sensorpool](private-sensor-pool.md)
</dt> <dt>

[Sensorpools](sensor-pools.md)
</dt> <dt>

[Systempoolverhalten](system-pool-behavior.md)
</dt> </dl>

 

 




