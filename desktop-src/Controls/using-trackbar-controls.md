---
title: Verwenden von Trackbar-Steuerelementen
description: Dieser Abschnitt enthält Implementierungsdetails und Beispiele für Trackbar-Steuerelemente.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b910c59121d692b45d122f9c38a5efdc74b1e9dd8eb47429327e5de34e9e4796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059370"
---
# <a name="using-trackbar-controls"></a>Verwenden von Trackbar-Steuerelementen

Dieser Abschnitt enthält Implementierungsdetails und Beispiele für Trackbar-Steuerelemente.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen einer Trackleiste](create-a-trackbar.md)<br/>                                           | Wenn die Trackleiste erstellt wird, werden sowohl der Bereich als auch der Auswahlbereich initialisiert. Die Seitengröße wird zu diesem Zeitpunkt ebenfalls festgelegt. <br/>                                                                                                                                           |
| [Verarbeiten von Trackbar-Benachrichtigungsmeldungen](process-trackbar-notification-messages.md)<br/> | Trackbars benachrichtigen ihr übergeordnetes Fenster über Benutzeraktionen, indem sie dem übergeordneten Element eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) senden. <br/>                                                                                                            |
| [Einschränken der Schiebereglerbewegung](limit-slider-movement.md)<br/>                                   | Wie unter Informationen zu [Trackbar-Steuerelementen](trackbar-controls.md)beschrieben, ist es möglich, einen Teil des Trackbarbereichs als Auswahlbereich festzulegen. Ein Zweck eines Auswahlbereichs kann darin sein, die Bewegung des Schiebereglers einzuschränken, sodass einige Teile des vollständigen Bereichs außerhalb der Grenzwerte liegen. <br/> |
| [Verwenden von Windows](use-buddy-windows.md)<br/>                                           | Indem Sie andere Steuerelemente als Fenster für eine Trackleiste festlegen, können Sie diese Steuerelemente automatisch als Bezeichnungen an den Enden der Trackleiste positionieren.<br/>                                                                                                                          |



 

 

 





