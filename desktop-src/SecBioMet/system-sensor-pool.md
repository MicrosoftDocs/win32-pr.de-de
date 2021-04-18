---
title: System Sensor Pool
description: Eine Auflistung von freigegeben-biometrischen Einheiten, die Zugriff auf die Windows-Authentifizierungsdienste bieten. Dieser Pool wird von Winlogon, UAC und einem beliebigen anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zuordnet.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae9487b91b57b2e9568817c92e44b4b7197f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337580"
---
# <a name="system-sensor-pool"></a>System Sensor Pool

Der System Sensor Pool ist eine Sammlung von shardbaren biometrischen Einheiten, die Zugriff auf die Windows-Authentifizierungsdienste bieten. Dieser Pool wird von Winlogon, UAC und einem beliebigen anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zuordnet. Biometrische Einheiten im System Pool:

-   Kann von mehreren Client Anwendungen gemeinsam genutzt werden.
-   Sendet Ereignis Hinweise, die durch den Abschluss biometrischer Vorgänge generiert werden, nur an die Anwendung mit dem aktuellen Fenster Fokus.
-   Verwenden Sie Konto-SIDs zur Darstellung der Vorlagen Identitäten. Alle Vorlagen, die einem einzelnen Benutzerkonto zugeordnet sind, werden mit der diesem Konto zugewiesenen sid markiert.
-   Abhängig vom vertrauenswürdigen Vorlagen Speicher, der vom Windows-biometrischen Dienst bereitgestellt wird.

Eine biometrische Einheit kann in den System Pool eingeschlossen werden, wenn dies der Fall sein kann:

-   Konfiguriert für den Betrieb im Standardmodus und fungiert nur als biometrisches Erfassungsgerät.
-   Konfiguriert für den Betrieb im erweiterten Modus, aber über keinen integrierten Vorlagen Speicher verfügt. Das heißt, der Speicher Adapter und der von Microsoft bereitgestellte Vorlagen Speicher müssen verwendet werden.
-   Die Konfiguration für den erweiterten Modus umfasst den integrierten Vorlagen Speicher und kann die erforderlichen Hashwerte generieren.

Wenn ein neues Sensorgerät angeschlossen ist, erstellt der Windows-biometrische Dienst eine biometrische Einheit dafür und versucht, diese Einheit für die Verwendung durch den systemsensorpool zu konfigurieren. Wenn die Konfiguration nicht erfolgreich ist, wird die biometrische Einheit in den nicht zugewiesenen Sensor Pool eingefügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Privater Sensor Pool](private-sensor-pool.md)
</dt> <dt>

[Sensor Pools](sensor-pools.md)
</dt> <dt>

[System Pool Verhalten](system-pool-behavior.md)
</dt> </dl>

 

 




