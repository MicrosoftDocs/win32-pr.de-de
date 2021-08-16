---
description: Einige Kommunikationsfunktionen können für ein Gerät mithilfe der EscapeCommFunction-Funktion aufgerufen werden.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Erweiterte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913feb46f61777bcb07fda1639519c4ef04fcb4905075b1c67955a3e911b9d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405335"
---
# <a name="extended-functions"></a>Erweiterte Funktionen

Einige Kommunikationsfunktionen können für ein Gerät mithilfe der [**EscapeCommFunction-Funktion aufgerufen**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) werden. Diese Funktion sendet einen Code, um das Gerät an die Ausführung einer erweiterten Funktion zu übergeben. Beispielsweise kann eine Anwendung die Zeichenübertragung mit dem SETBREAK-Code ansetzen und die Übertragung mit dem CLRBREAK-Code fortsetzen. Diese speziellen Vorgänge können auch durch Aufrufen der [**Funktionen SetCommBreak und**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) [**ClearCommBreak gestartet**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) werden. **EscapeCommFunction kann** auch verwendet werden, um die manuelle Modemsteuerung zu implementieren. Beispielsweise können die CLRDTR- und SETDTR-Codes verwendet werden, um die manuelle DTR-Flusssteuerung (data-terminal-ready) zu implementieren. Beachten Sie jedoch, dass ein Fehler auftritt, wenn ein Prozess **EscapeCommFunction** verwendet, um die DTR-Zeile zu bearbeiten, wenn das Gerät zum Aktivieren des DTR-Handshakes konfiguriert wurde, oder die RTS-Zeile (Request-to-Send), wenn RTS-Handshaking aktiviert ist.

Die [**DeviceIoControl-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) ermöglicht es einem Prozess, einen erweiterten Funktionscode direkt an einen angegebenen Gerätetreiber zu senden, wodurch das Gerät einen bestimmten Vorgang ausführen kann. **DeviceIoControl stellt** ein Gerät bereit, das einer Kommunikationsressource zugeordnet ist und von den standardmäßigen seriellen Kommunikationsfunktionen nicht unterstützt wird. Sie ermöglicht es einer Anwendung, ein Gerät mit parametern zu konfigurieren, die für dieses Gerät eindeutig sind, und gerätespezifische Funktionen auf aufruft.

 

 
