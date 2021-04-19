---
description: Die iinstallationprogress-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Iinstallationprogress-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353108"
---
# <a name="iinstallationprogress-properties"></a>Iinstallationprogress-Eigenschaften

Die [**iinstallationprogress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                   | BESCHREIBUNG                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currentupdateingedex**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | Ruft einen NULL basierten Indexwert ab, der das Update angibt, das zurzeit installiert oder deinstalliert wird, wenn mehrere Updates ausgewählt wurden. |
| [**Currentupdateprozentucomplete**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | Ruft ab, wie weit der Installations-oder der deinstalstallvorgang für das aktuelle Update in Prozent erreicht wurde.                                    |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | Ruft ab, wie weit der gesamte Installations-oder Deinstallationsprozess als Prozentsatz fortgeschritten ist.                                                   |



 

 

 



