---
title: DRM-Netzwerkvorgänge
description: DRM-Netzwerkvorgänge
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Medienformat-SDK, DRM-Netzwerkvorgänge
- Advanced Systems Format (ASF), DRM-Netzwerkvorgänge
- ASF (Advanced Systems Format), DRM-Netzwerkvorgänge
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Netzwerkvorgänge
- DRM (Digital Rights Management), Netzwerkbetrieb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f026ed972b88a1e6290bdd513012c2fab758da2c5b4b91a6a1162df5d258207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771750"
---
# <a name="drm-network-operations"></a>DRM-Netzwerkvorgänge

Für mehrere DRM-bezogene Vorgänge muss Ihre Anwendung eine Verbindung mit einem Dienst herstellen, der in einem Netzwerk ausgeführt wird. Zu diesen Vorgängen gehören Individualisierung, Lizenzerwerb, Lizenzsperrung und Lizenzsicherung und -wiederherstellung.

Wie bei jeder Netzwerktransaktion sollte Ihre Anwendung eine Vielzahl von Schwierigkeiten beim Einarbeiten von Features berücksichtigen, die Netzwerkvorgänge erfordern. Ihre Anwendung sollte den Status des Vorgangs in jedem Umfang nachverfolgen, der für das spezifische Feature möglich ist, in der Regel durch Die Behandlung von Statusmeldungen. Sie sollten dem Benutzer Feedback zum Status geben. Wenn ein Vorgang beim ersten Versuch fehlschlägt, sollten Sie dem Benutzer die Möglichkeit geben, den Vorgang erneut zu versuchen. In vielen Fällen ist der erste Versuch schwierig, aber ein nachfolgender Versuch wird ohne Fehler abgeschlossen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




