---
description: Die IInstallationProgress-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: IInstallationProgress-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c688694be4a791c8d3ec861cc66367ebf89922817076032527f5458e0645918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130512"
---
# <a name="iinstallationprogress-properties"></a>IInstallationProgress-Eigenschaften

Die [**IInstallationProgress-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                   | Beschreibung                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | Ruft einen nullbasierten Indexwert ab, der das Update angibt, das gerade installiert oder deinstalliert wird, wenn mehrere Updates ausgewählt wurden. |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | Ruft als Prozentsatz ab, wie weit der Installations- oder Deinstallationsprozess für das aktuelle Update fortgeschritten ist.                                    |
| [**Percentcomplete**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | Ruft als Prozentsatz ab, wie weit der gesamte Installations- oder Deinstallationsvorgang fortgeschritten ist.                                                   |



 

 

 



