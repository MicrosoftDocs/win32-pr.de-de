---
title: Bei gekachelten Ressourcen werden keine Schablonen Formate unterstützt.
description: Formate mit Schablonen werden bei gekachelten Ressourcen nicht unterstützt.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036241"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>Bei gekachelten Ressourcen werden keine Schablonen Formate unterstützt.

Formate mit Schablonen werden bei gekachelten Ressourcen nicht unterstützt.

Zu den Formaten, die die Schablone enthalten, gehören DXGI \_ \_ -Format D24 \_ unorm \_ S8 \_ uint (und Verwandte Formate in der R24G8-Familie) und DXGI- \_ Format \_ d32 \_ float \_ S8X24 \_ uint (und Verwandte Formate in der R32G8X24-Familie).

Einige Implementierungen speichern Tiefe und Schablone in separaten Zuordnungen, während andere diese in anderen speichern. Die Kachel Verwaltung für die beiden Schemas müsste anders sein, und die Unterschiede können von keiner einzelnen API abstrahiert oder rationalisiert werden. Für zukünftige Hardware wird die Unterstützung unabhängiger tiefen und Schablonen Oberflächen empfohlen, die jeweils unabhängig voneinander nebeneinander angeordnet sind. die 32-Bit-Tiefe hätte 128 x 128 Kacheln, und die 8-Bit-Schablone hätte 256 x 256 Kacheln. Daher müssten Anwendungen mit einer Fehlausrichtung der Kachel Form zwischen Tiefe und Schablone Leben. Das gleiche Problem ist jedoch bereits mit verschiedenen renderzieloberflächen-Formaten vorhanden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Prozessübergreifende Ressourcen übergreifende und Geräte Freigabe](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




