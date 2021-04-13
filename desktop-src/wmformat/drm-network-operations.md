---
title: DRM-Netzwerk Vorgänge
description: DRM-Netzwerk Vorgänge
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media-Format-SDK, DRM-Netzwerk Vorgänge
- Advanced Systems Format (ASF), DRM-Netzwerk Vorgänge
- ASF (Advanced Systems Format), DRM-Netzwerk Vorgänge
- Digital Rights Management (DRM), Netzwerk Vorgänge
- DRM (Digital Rights Management), Netzwerk Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309387"
---
# <a name="drm-network-operations"></a>DRM-Netzwerk Vorgänge

Mehrere DRM-bezogene Vorgänge erfordern, dass Ihre Anwendung eine Verbindung mit einem Dienst herstellt, der in einem Netzwerk ausgeführt wird. Zu diesen Vorgängen gehören die Personalisierung, der Lizenzerwerb, die Lizenz Sperrung und die Lizenz Sicherung und-Wiederherstellung.

Wie bei jeder Netzwerk Transaktion sollte Ihre Anwendung eine Vielzahl von Schwierigkeiten berücksichtigen, wenn Sie Features einschließen, für die Netzwerk Vorgänge erforderlich sind. Die Anwendung sollte den Status des Vorgangs bis zu dem für das jeweilige Feature möglichen Umfang nachverfolgen, normalerweise durch die Verarbeitung von Statusmeldungen. Sie sollten dem Benutzer Feedback zum Status geben. Wenn beim ersten Versuch ein Vorgang fehlschlägt, sollten Sie dem Benutzer die Möglichkeit geben, den Vorgang zu wiederholen. In vielen Fällen tritt beim ersten Versuch eine Schwierigkeit auf, ein nachfolgende Versuch wird jedoch ohne Fehler abgeschlossen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




