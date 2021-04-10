---
description: Einige Kommunikationsfunktionen können mithilfe der escapecommfunction-Funktion für ein Gerät aufgerufen werden.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Erweiterte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041484"
---
# <a name="extended-functions"></a>Erweiterte Funktionen

Einige Kommunikationsfunktionen können mithilfe der [**escapecommfunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) -Funktion für ein Gerät aufgerufen werden. Diese Funktion sendet einen Code, um das Gerät an die Ausführung einer erweiterten Funktion weiterzuleiten. Beispielsweise kann eine Anwendung die Zeichen Übertragung mit dem setbreak-Code aussetzen und die Übertragung mit dem clrbreak-Code fortsetzen. Diese speziellen Vorgänge können auch gestartet werden, indem die Funktionen [**setcommbreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) und [**clearcommbreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) aufgerufen werden. **Escapecommfunction** kann auch verwendet werden, um Manuelles Modem Steuerelement zu implementieren. Beispielsweise können die Codes clrdtr und setdtr zum Implementieren der manuellen DTR-Fluss Steuerung (Data-Terminal-Ready) verwendet werden. Beachten Sie jedoch, dass ein Fehler auftritt, wenn ein Prozess **escapecommfunction** zum Bearbeiten der DTR-Zeile verwendet, wenn das Gerät für die Aktivierung von DTR-Handshake konfiguriert wurde, oder die RTS-Zeile (Anforderungs-zu-Send-Zeile), wenn der RTS-Handler aktiviert ist.

Die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) ermöglicht einem Prozess, einen erweiterten Funktionscode direkt an einen angegebenen Gerätetreiber zu senden, wodurch das Gerät einen bestimmten Vorgang ausführt. **DeviceIoControl** gibt ein Gerät an, das den Kommunikationsressourcen Funktionen zugeordnet ist, die von den standardmäßigen seriellen Kommunikationsfunktionen nicht unterstützt werden. Sie ermöglicht es einer Anwendung, ein Gerät mithilfe von für dieses Gerät eindeutigen Parametern zu konfigurieren und gerätespezifische Funktionen aufzurufen.

 

 
