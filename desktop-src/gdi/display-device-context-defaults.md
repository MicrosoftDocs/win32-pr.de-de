---
description: Beim ersten Erstellen eines Anzeigegeräte Kontexts weist das System Standardwerte für die Attribute (d. h. das Zeichnen von Objekten, Farben und Modi) zu, die den Gerätekontext bilden.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Gerätekontext Standardwerte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8abcf79339d4f1cc158253d46cc3eb02ec41311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863659"
---
# <a name="display-device-context-defaults"></a>Gerätekontext Standardwerte anzeigen

Beim ersten Erstellen eines Anzeigegeräte Kontexts weist das System Standardwerte für die Attribute (d. h. das Zeichnen von Objekten, Farben und Modi) zu, die den Gerätekontext bilden. In der folgenden Tabelle werden die Standardwerte für die Attribute eines Anzeigegeräte Kontexts angezeigt.



| attribute                             | Standardwert                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Hintergrundfarbe                      | Einstellung für die Hintergrundfarbe in der Systemsteuerung (in der Regel weiß).                                                                               |
| Hintergrundmodus                       | Lässige                                                                                                                                        |
| Bitmap                                | Keine                                                                                                                                          |
| Brush                                 | weißer \_ Pinsel                                                                                                                                  |
| Pinsel Ursprung                          | (0,0)                                                                                                                                         |
| Clippingbereich                       | Das gesamte Fenster oder der Client Bereich mit dem ausgeschnittenen Aktualisierungs Bereich. Untergeordnete und Popup Fenster im Client Bereich können ebenfalls abgeschnitten werden. |
| Palette                               | Standard \_ Palette                                                                                                                              |
| Aktuelle Stift Position                  | (0,0)                                                                                                                                         |
| Geräte Ursprung                         | Obere linke Ecke des Fensters oder des Client Bereichs.                                                                                           |
| Zeichnungsmodus                          | R2- \_ CopyPen                                                                                                                                   |
| Schriftart                                  | System \_ Schriftart                                                                                                                                  |
| Intercharacter-Abstand                | 0                                                                                                                                             |
| Mapping-Modus                          | MM- \_ Text                                                                                                                                      |
| Stift                                   | Schwarzer \_ Stift                                                                                                                                    |
| [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) Füll Modus | Nder                                                                                                                                     |
| Streckungs Modus                          | Blackonwhite                                                                                                                                  |
| Textfarbe                            | Textfarb Einstellung in der Systemsteuerung (in der Regel Schwarz).                                                                                     |
| Viewportblock                       | (1, 1)                                                                                                                                         |
| Der Viewportursprung                       | (0,0)                                                                                                                                         |
| Fensterblock                         | (1, 1)                                                                                                                                         |
| Fenster Ursprung                         | (0,0)                                                                                                                                         |



 

Eine Anwendung kann die Werte der Anzeigegeräte Kontext Attribute mithilfe von Auswahl-und Attribut Funktionen ändern, wie z. b. [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)und [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor). Beispielsweise kann eine Anwendung die Standard Maßeinheiten im Koordinatensystem ändern, indem **setmapmode** verwendet wird, um den Zustellungs Modus zu ändern.

Änderungen an den Attributwerten eines gemeinsamen, übergeordneten oder Fenster Geräte Kontexts sind nicht permanent. Wenn eine Anwendung diese Geräte Kontexte freigibt, gehen die aktuellen Auswahlen (z. b. Zustellungs Modus und Clippingbereich) verloren, wenn der Kontext an den Cache zurückgegeben wird. Änderungen an Klassen-oder privaten Geräte Kontexten bleiben unbegrenzt erhalten. Um die ursprünglichen Standardwerte wiederherzustellen, muss eine Anwendung jedes Attribut explizit festlegen.

 

 



