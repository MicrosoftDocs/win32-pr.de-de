---
description: Die Microsoft-erkenungen verwenden die folgenden GUIDs.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: Eigenschafts-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132028"
---
# <a name="property-guids"></a>Eigenschafts-GUIDs

Die Microsoft-erkenungen verwenden die folgenden GUIDs. Wenn möglich sollten diese GUIDs von Anwendungen verwendet werden. Es wird jedoch erwartet und empfohlen, dass andere erkenungen zusätzliche GUIDs für Eigenschaften verwenden, die nicht von den Microsoft-erkenungen unterstützt werden.

Alle Eigenschafts Funktionen wurden mit dem Verständnis entwickelt, dass die Liste der GUIDs von anderen Erkennungs Modulen erweitert werden kann. Diese Eigenschafts Funktionen umfassen Folgendes:

-   [**Getcontextpropertylist-Funktion**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**Getcontextpropertyvalue-Funktion**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**Getresultpropertylist-Funktion**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**Setcontextpropertyvalue-Funktion**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

In der folgenden Tabelle sind die in "msink AUT. h" (installiert in c: \\ Programme \\ Microsoft Tablet PC Platform SDK standardmäßig installierten Tablet PC-Eigenschafts-GUIDs \\ ) aufgeführt.



| GUID                                                  | Definition                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| inkrecognitionproperty- \_ boxnumber<br/>          | Der Index für die Alternative Box-Erkennung im Box-Modus<br/>                                    |
| inkrecognitionproperty ( \_ LineNumber)<br/>         | Die Zeilennummer<br/>                                                                   |
| inkrecognitionproperty- \_ Segmentierung<br/>       | Segmentierung von Wörtern und Zeichen durch die Erkennung<br/>                                  |
| inkrecognitionproperty- \_ Hotpoint<br/>           | Der heiß Punkt der Bewegung<br/>                                                             |
| inkrecognitionproperty \_ MaximumStrokeCount<br/> | Maximale Anzahl von Strichen für ein Segment<br/>                                           |
| inkrecognitionproperty- \_ PointsPerInch<br/>      | Die Metrik "Punkte pro Zoll"<br/>                                                        |
| inkrecognitionproperty \_ conficelevel<br/>    | [**Vertrauen \_ Level**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) -Enumeration<br/>                         |
| inkrecognitionproperty- \_ LineMetrics<br/>        | Informationen zum Berechnen von Baseline, Mittelpunkt oder beidem, die im Gitter verwendet werden.<br/> |



 

 

 




