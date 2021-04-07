---
title: System Einträge für Kompressoren, Debug-und Renderer
description: System Einträge für Kompressoren, Debug-und Renderer
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Video für Windows (Vfw), Systemeinträge für den Kompressor
- VFW (Video für Windows), Systemeinträge für den Kompressor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713301"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>System Einträge für Kompressoren, Debug-und Renderer

Das System verwendet Einträge in der Registrierung, um VCM-Treiber zu suchen. Diese Einträge sind in Form von 2 4-Zeichen Codes, die durch einen Zeitraum voneinander getrennt sind. Der erste Code, der aus vier Zeichen besteht, wird vom System definiert und kann eine der folgenden sein:



| Code mit vier Zeichen | BESCHREIBUNG                               |
|---------------------|-------------------------------------------|
| VIDC              | Identifiziert die-Kompressoren und-Debug-Geräte. |
| "Vids"              | Identifiziert videostreamrenderer.        |
| "Txts"              | Identifiziert textstreamrenderer.         |
| Au              | Identifiziert audiostreamhandler.         |



 

Benutzerdefinierte Renderer können Ihre eigenen vier Zeichen Codes definieren.

Der zweite Code mit vier Zeichen wird vom Treiber definiert. In der Regel entspricht der zweite aus vier Zeichen bestehende Code dem Datentyp, der vom Treiber verarbeitet werden kann.

Beim Öffnen eines VCM-Treibers gibt eine Anwendung den Typ des Treibers und den Typ des benötigten Daten Handlers an. Diese Informationen stammen in der Regel aus dem Datenstrom Header. Das System versucht, den angegebenen Daten Handler zu öffnen. wenn er jedoch fehlschlägt, durchsucht das System die Registrierung nach einem Treiber, der über den erforderlichen Handler verfügt.

Bei der Suche nach dem Treiber versucht das System, die vier Zeichen Codes, die für den Treibertyp und den Daten Handler angegeben sind, mit den im Treiber Eintrag angegebenen Zeichen zu vergleichen. Wenn eine Anwendung z. b. den mssq-Kompressor angibt, durchsucht das System die Registrierung nach dem Treiber Eintrag "VIDC. mssq". Wenn eine Übereinstimmung nicht gefunden werden kann, öffnet Sie jeden Treiber, der dem Treibertyp entspricht, und sucht einen, der den Typ der von der Anwendung festgelegten Daten verarbeiten kann. Wenn das System z. b. "VIDC. mssq" nicht finden konnte, werden alle Treiber mit dem vierstelligen Code "VIDC" geöffnet, und Sie finden einen, der die Daten verarbeiten kann.

 

 




