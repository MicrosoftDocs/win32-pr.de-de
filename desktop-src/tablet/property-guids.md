---
description: Die Microsoft-Recognizer verwenden die folgenden GUIDs.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: Eigenschaften-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4883ee713122ae36c4ad7e29b86013beb670545ffac31da28bad4da8c2f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031658"
---
# <a name="property-guids"></a>Eigenschaften-GUIDs

Die Microsoft-Recognizer verwenden die folgenden GUIDs. Nach Möglichkeit sollten Anwendungen diese GUIDs verwenden. Es wird jedoch erwartet und empfohlen, dass andere Recognizer zusätzliche GUIDs für Eigenschaften verwenden, die von den Microsoft-Recognizern nicht unterstützt werden.

Alle Eigenschaftenfunktionen wurden mit dem Verständnis entwickelt, dass die Liste der GUIDs durch andere Erkennen erweitert werden kann. Zu diesen Eigenschaftenfunktionen gehören:

-   [**GetContextPropertyList-Funktion**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**GetContextPropertyValue-Funktion**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**GetResultPropertyList-Funktion**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**SetContextPropertyValue-Funktion**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

In der folgenden Tabelle sind die guiDs der Tablet PC-Eigenschaften aufgeführt, die in msinkaut.h definiert sind (installiert in c: \\ Programme Microsoft Tablet PC Platform SDK Include \\ \\ standardmäßig).



| GUID                                                  | Definition                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | Der Alternative Feldindex der Wiedererkennung im Feldmodus<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | Die Zeilennummer<br/>                                                                   |
| INKRECOGNITIONPROPERTY-SEGMENTIERUNG \_<br/>       | Segmentieren von Wörtern und Zeichen durch die Wiedererkennung<br/>                                  |
| INKRECOGNITIONPROPERTY \_ HOTPOINT<br/>           | Der Gesten-Hot point<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | Maximale Anzahl von Strichen für ein Segment<br/>                                           |
| INKRECOGNITIONPROPERTY-PUNKTEPERINCH \_<br/>      | Die Punkt-pro-Zoll-Metrik<br/>                                                        |
| INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL<br/>    | [**VERTRAUEN \_ LEVEL-Enumeration**](/windows/win32/api/rectypes/ne-rectypes-confidence_level)<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | Informationen zum Berechnen der Baseline, der Midline oder beides, die im Lattice verwendet werden<br/> |



 

 

 




