---
title: Statusanzeige
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Statusanzeige-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c9cd66326336cd3733f881f3f19d82fedc3bf8d8420f83035bf20dc914c7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670651"
---
# <a name="progress-bar"></a>Statusanzeige

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit Statusanzeige-Steuerelementen verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                            | Inhalte                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Statusanzeige-Steuerelement](progress-bar-control.md) | Eine Statusanzeige ist ein Fenster, das eine Anwendung verwenden kann, um den Fortschritt eines längeren Vorgangs anzugeben.<br/> |



 

### <a name="messages"></a>Meldungen



| Thema                                       | Inhalte                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBM \_ DELTAPOS**](pbm-deltapos.md)       | Erhöht die aktuelle Position einer Statusanzeige um ein angegebenes Inkrement und gezeichnet den Balken neu, um die neue Position widerzuspiegeln. <br/>                                                                                                                                 |
| [**PBM \_ GETBARCOLOR**](pbm-getbarcolor.md) | Ruft die Farbe der Statusanzeige ab.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETBKCOLOR**](pbm-getbkcolor.md)   | Ruft die Hintergrundfarbe der Statusanzeige ab.<br/>                                                                                                                                                                                                             |
| [**PBM \_ GETPOS**](pbm-getpos.md)           | Ruft die aktuelle Position der Statusanzeige ab. <br/>                                                                                                                                                                                                       |
| [**PBM \_ GETRANGE**](pbm-getrange.md)       | Ruft Informationen zu den aktuellen hohen und niedrigen Grenzwerten eines bestimmten Statusanzeige-Steuerelements ab. <br/>                                                                                                                                                              |
| [**PBM \_ GETSTATE**](pbm-getstate.md)       | Ruft den Status der Statusanzeige ab.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETSTEP**](pbm-getstep.md)         | Ruft das Schrittinkrement für eine Statusanzeige ab. Das Schrittinkrement ist der Betrag, um den die Statusanzeige ihre aktuelle Position erhöht, wenn sie eine [**PBM \_ STEPIT-Nachricht**](pbm-stepit.md) empfängt.<br/>                                               |
| [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) | Legt die Farbe der Statusanzeigeleiste im Statusanzeige-Steuerelement fest. <br/>                                                                                                                                                                                 |
| [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md)   | Legt die Hintergrundfarbe in der Statusleiste fest. <br/>                                                                                                                                                                                                            |
| [**PBM \_ SETMARQUEE**](pbm-setmarquee.md)   | Legt die Statusanzeige auf den Festlaufmodus fest. Dies bewirkt, dass sich die Statusanzeige wie ein Marquee bewegt.<br/>                                                                                                                                                                |
| [**PBM \_ SETPOS**](pbm-setpos.md)           | Legt die aktuelle Position für eine Statusanzeige fest und zeichnet die Leiste neu, um die neue Position widerzuspiegeln. <br/>                                                                                                                                                             |
| [**PBM \_ SETRANGE**](pbm-setrange.md)       | Legt die Minimal- und Höchstwerte für eine Statusanzeige fest und zeichnet die Leiste neu, um den neuen Bereich widerzuspiegeln.<br/>                                                                                                                                                       |
| [**PBM \_ SETRANGE32**](pbm-setrange32.md)   | Legt den Bereich eines Statusanzeige-Steuerelements auf einen 32-Bit-Wert fest. <br/>                                                                                                                                                                                               |
| [**PBM \_ SETSTATE**](pbm-setstate.md)       | Legt den Status der Statusanzeige fest.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ SETSTEP**](pbm-setstep.md)         | Gibt das Schrittinkrement für eine Statusanzeige an. Das Schrittinkrement ist der Betrag, um den die Statusanzeige ihre aktuelle Position erhöht, wenn sie eine [**PBM \_ STEPIT-Nachricht**](pbm-stepit.md) empfängt. Standardmäßig ist das Schrittinkrement auf 10 festgelegt. <br/> |
| [**PBM \_ STEPIT**](pbm-stepit.md)           | Erhöht die aktuelle Position für eine Statusanzeige um den Schrittinkrement und gezeichnet den Balken neu, um die neue Position widerzuspiegeln. Eine Anwendung legt das Schrittinkrement fest, indem die [**PBM \_ SETSTEP-Nachricht**](pbm-setstep.md) gesendet wird. <br/>                                |



 

### <a name="structures"></a>Strukturen



| Thema                      | Inhalte                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Enthält Informationen zu den hohen und niedrigen Grenzwerten eines Statusanzeige-Steuerelements. Diese Struktur wird mit der [**PBM \_ GETRANGE-Nachricht**](pbm-getrange.md) verwendet. <br/> |



 

### <a name="constants"></a>Konstanten



| Thema                                                          | Inhalte                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Statusleisten-Steuerelementstile](progress-bar-control-styles.md) | Die folgenden Steuerelementstile werden von **Progress Bar-Steuerelementen** unterstützt:<br/> |



 

 

 





