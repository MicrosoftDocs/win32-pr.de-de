---
title: Statusanzeige
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Statusanzeige-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b99a31bbbd3b80de0d528d5232c79c28af1e1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338576"
---
# <a name="progress-bar"></a>Statusanzeige

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Statusanzeige-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                            | Inhalte                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Statusanzeige-Steuerelement](progress-bar-control.md) | Eine Statusanzeige ist ein Fenster, mit dem eine Anwendung den Fortschritt eines langwierigen Vorgangs angeben kann.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                       | Inhalte                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBM-Delta Torys \_**](pbm-deltapos.md)       | Verschiebt die aktuelle Position einer Statusleiste um ein angegebenes Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln. <br/>                                                                                                                                 |
| [**PBM \_ getbarcolor**](pbm-getbarcolor.md) | Ruft die Farbe der Statusanzeige ab.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GetBkColor**](pbm-getbkcolor.md)   | Ruft die Hintergrundfarbe der Statusanzeige ab.<br/>                                                                                                                                                                                                             |
| [**PBM- \_ GetPos**](pbm-getpos.md)           | Ruft die aktuelle Position der Statusanzeige ab. <br/>                                                                                                                                                                                                       |
| [**PBM- \_ GetRange**](pbm-getrange.md)       | Ruft Informationen über die aktuellen höchst-und tiefstgrenzen eines angegebenen Statusanzeige-Steuer Elements ab. <br/>                                                                                                                                                              |
| [**PBM \_ GetState**](pbm-getstate.md)       | Ruft den Status der Statusanzeige ab.<br/>                                                                                                                                                                                                                        |
| [**PBM- \_ getstep**](pbm-getstep.md)         | Ruft das Schritt Inkrement für eine Statusanzeige ab. Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer [**PBM- \_ StepIt**](pbm-stepit.md) -Nachricht die aktuelle Position vergrößert.<br/>                                               |
| [**PBM \_ setbarcolor**](pbm-setbarcolor.md) | Legt die Farbe der Statusanzeige Leiste im Statusanzeige-Steuerelement fest. <br/>                                                                                                                                                                                 |
| [**PBM \_ SetBkColor**](pbm-setbkcolor.md)   | Legt die Hintergrundfarbe in der Statusanzeige fest. <br/>                                                                                                                                                                                                            |
| [**PBM \_ setmarquee**](pbm-setmarquee.md)   | Legt die Statusanzeige auf den Marquee-Modus fest. Dies bewirkt, dass die Statusanzeige wie ein Marquee verschoben wird.<br/>                                                                                                                                                                |
| [**PBM- \_ SetPos**](pbm-setpos.md)           | Legt die aktuelle Position für eine Statusanzeige fest und zeichnet den Balken neu, um die neue Position widerzuspiegeln. <br/>                                                                                                                                                             |
| [**PBM-über \_ Tragung**](pbm-setrange.md)       | Legt den minimalen und maximalen Wert für eine Statusanzeige fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.<br/>                                                                                                                                                       |
| [**PBM \_ SETRANGE32**](pbm-setrange32.md)   | Legt den Bereich eines Statusanzeige-Steuer Elements auf einen 32-Bit-Wert fest. <br/>                                                                                                                                                                                               |
| [**PBM- \_ SetState**](pbm-setstate.md)       | Legt den Status der Statusanzeige fest.<br/>                                                                                                                                                                                                                        |
| [**PBM- \_ SetStep**](pbm-setstep.md)         | Gibt das Schritt Inkrement für eine Statusanzeige an. Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer [**PBM- \_ StepIt**](pbm-stepit.md) -Nachricht die aktuelle Position vergrößert. Standardmäßig ist das Schritt Inkrement auf 10 festgelegt. <br/> |
| [**PBM- \_ StepIt**](pbm-stepit.md)           | Verschiebt die aktuelle Position für eine Statusanzeige um das Schritt Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln. Eine Anwendung legt das Schritt Inkrement fest, indem die [**PBM- \_ SetStep**](pbm-setstep.md) -Nachricht gesendet wird. <br/>                                |



 

### <a name="structures"></a>Strukturen



| Thema                      | Inhalte                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pbrange**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Enthält Informationen zu den höchst-und tiefstgrenzen eines Statusanzeige-Steuer Elements. Diese Struktur wird mit der [**PBM- \_ GetRange**](pbm-getrange.md) -Nachricht verwendet. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                                          | Inhalte                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Stile der Statusanzeige-Steuerelemente](progress-bar-control-styles.md) | Die folgenden Steuerelement Stile werden von den **Status** Anzeige-Steuerelementen unterstützt:<br/> |



 

 

 





