---
description: Beim ersten Erstellen eines Anzeigegerätekontexts weist das System Standardwerte für die Attribute (d. h. Zeichnungsobjekte, Farben und Modi) zu, aus denen der Gerätekontext besteht.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Anzeigen von Gerätekontextstandardeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366c4ecb861b64d2b69836832259e6820e0f8809e4aa478d074220d133ccec55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887277"
---
# <a name="display-device-context-defaults"></a>Anzeigen von Gerätekontextstandardeinstellungen

Beim ersten Erstellen eines Anzeigegerätekontexts weist das System Standardwerte für die Attribute (d. h. Zeichnungsobjekte, Farben und Modi) zu, aus denen der Gerätekontext besteht. Die folgende Tabelle zeigt die Standardwerte für die Attribute eines Anzeigegerätekontexts.



| attribute                             | Standardwert                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Hintergrundfarbe                      | Einstellung der Hintergrundfarbe aus Systemsteuerung (in der Regel weiß).                                                                               |
| Hintergrundmodus                       | Undurchsichtig                                                                                                                                        |
| Bitmap                                | Keine                                                                                                                                          |
| Brush                                 | WEIßER \_ PINSEL                                                                                                                                  |
| Pinselursprung                          | (0,0)                                                                                                                                         |
| Beschneidungsregion                       | Das gesamte Fenster oder der gesamte Clientbereich, in dem der Updatebereich nach Bedarf abgeschnitten ist. Untergeordnete und Popupfenster im Clientbereich können ebenfalls abgeschnitten werden. |
| Palette                               | \_STANDARDPALETTE                                                                                                                              |
| Aktuelle Stiftposition                  | (0,0)                                                                                                                                         |
| Geräteursprung                         | Obere linke Ecke des Fensters oder des Clientbereichs.                                                                                           |
| Zeichnungsmodus                          | R2 \_ COPYPEN                                                                                                                                   |
| Schriftart                                  | \_SYSTEMSCHRIFTART                                                                                                                                  |
| Intercharacter-Abstand                | 0                                                                                                                                             |
| Zuordnungsmodus                          | MM \_ TEXT                                                                                                                                      |
| Stift                                   | BLACK \_ PEN                                                                                                                                    |
| [](/windows/desktop/api/Wingdi/nf-wingdi-polygon) Polygon-Füllmodus | Alternative                                                                                                                                     |
| Stretchmodus                          | BLACKONWHITE                                                                                                                                  |
| Textfarbe                            | Einstellung der Textfarbe aus Systemsteuerung (in der Regel Schwarz).                                                                                     |
| Viewport-Erweiterung                       | (1,1)                                                                                                                                         |
| Viewportursprung                       | (0,0)                                                                                                                                         |
| Fensterumfang                         | (1,1)                                                                                                                                         |
| Fensterursprung                         | (0,0)                                                                                                                                         |



 

Eine Anwendung kann die Werte der Anzeigegerätekontextattribute mithilfe von Auswahl- und Attributfunktionen wie [**SelectObject,**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)und [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)ändern. Beispielsweise kann eine Anwendung die Standardmaßeinheiten im Koordinatensystem ändern, indem **Sie SetMapMode** verwenden, um den Zuordnungsmodus zu ändern.

Änderungen an den Attributwerten eines allgemeinen, übergeordneten oder Fenstergerätekontexts sind nicht dauerhaft. Wenn eine Anwendung diese Gerätekontexte freigibt, gehen die aktuellen Auswahlen, z. B. Zuordnungsmodus und Clippingbereich, verloren, wenn der Kontext an den Cache zurückgegeben wird. Änderungen an einem Klassen- oder privaten Gerätekontext bleiben unbegrenzt erhalten. Um sie auf die ursprünglichen Standardwerte wiederherzustellen, muss eine Anwendung jedes Attribut explizit festlegen.

 

 



