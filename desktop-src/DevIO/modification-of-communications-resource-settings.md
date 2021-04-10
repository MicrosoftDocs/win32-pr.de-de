---
description: Wenn die Funktion "comatefile" ein Handle für eine serielle Kommunikations Ressource öffnet, initialisiert und konfiguriert das System die Ressource entsprechend den Werten, die beim letzten Öffnen der Ressource festgelegt wurden.
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: Änderung der Kommunikationsressourcen Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8658029470fae9ee2d70ffb1459312c3c4d80ecf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041430"
---
# <a name="modification-of-communications-resource-settings"></a>Änderung der Kommunikationsressourcen Einstellungen

Wenn die Funktion " [**comatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " ein Handle für eine serielle Kommunikations Ressource öffnet, initialisiert und konfiguriert das System die Ressource entsprechend den Werten, die beim letzten Öffnen der Ressource festgelegt wurden. Wenn Sie die vorherigen Einstellungen beibehalten, kann der Benutzer die Einstellungen beibehalten, die **durch einen** modusbefehl angegeben werden, wenn das Gerät erneut geöffnet wird. Die Werte, die vom vorherigen Öffnungsvorgang geerbt wurden, umfassen die Konfigurationseinstellungen des Geräte Kontroll Blocks (eine [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur) und die Timeout Werte, die bei e/a-Vorgängen verwendet werden. Wenn das Gerät noch nie geöffnet wurde, wird es mit den Standardeinstellungen des Systems konfiguriert.

Um die anfängliche Konfiguration einer seriellen Kommunikations Ressource zu ermitteln, Ruft ein Prozess die [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) -Funktion auf, die eine [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur des seriellen Anschlusses mit den aktuellen Konfigurationseinstellungen füllt. Um diese Konfiguration zu ändern, gibt ein Prozess eine **DCB** -Struktur in einem Aufrufen der [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) -Funktion an.

Member der [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur geben die Konfigurationseinstellungen an, z. b. die Baudrate, die Anzahl der Datenbits pro Byte und die Anzahl von Stoppbits pro Byte. Andere **DCB** -Member geben Sonderzeichen an und aktivieren die Paritäts Überprüfung und Fluss Steuerung. Wenn ein Prozess nur einige dieser Konfigurationseinstellungen ändern muss, sollte zuerst [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) aufgerufen werden, um eine **DCB** -Struktur mit der aktuellen Konfiguration auszufüllen. Anschließend kann der Prozess die wichtigen Werte in der **DCB** -Struktur anpassen und das Gerät neu konfigurieren, indem [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) aufgerufen und die geänderte **DCB** -Struktur angegeben wird. Diese Prozedur stellt sicher, dass die unveränderten Member der **DCB** -Struktur entsprechende Werte enthalten. Ein häufiger Fehler ist beispielsweise die Konfiguration eines Geräts mit einer **DCB** -Struktur, in der das **XonChar** -Element der Struktur gleich dem **XoffChar** -Member ist.

Die [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba) -Funktion bietet eine weitere Möglichkeit zum Ändern einer [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur. **BuildCommDCB** verwendet eine Zeichenfolge mit derselben Form wie die Befehlszeilenargumente des **Modus** -Befehls, um die Baudrate, das Paritäts Schema, die Anzahl der Stoppbits und die Anzahl der Datenbits anzugeben. Die verbleibenden [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Member werden von dieser Funktion nicht geändert, mit der Ausnahme, dass die entsprechenden Member so festgelegt sind, dass XON/XOFF und die Hardware Fluss Steuerung deaktiviert werden. **BuildCommDCB** ändert nur eine **DCB** -Struktur. das Gerät wird nicht neu konfiguriert.

Ein Prozess kann eine Kommunikations Ressource neu konfigurieren, indem Sie die [**getcommproperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) -Funktion verwendet, um Informationen von einem Gerätetreiber zu den unterstützten Konfigurationseinstellungen zu erhalten. Der Prozess kann diese Informationen verwenden, um zu vermeiden, dass eine nicht unterstützte Konfiguration angegeben wird.

Die Funktion " [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) " konfiguriert die Kommunikations Ressource neu, wirkt sich jedoch nicht auf die interne Ausgabe und die Eingabepuffer des angegebenen Treibers aus. Die Puffer werden nicht geleert, und ausstehende Lese-und Schreibvorgänge werden nicht vorzeitig beendet.

Ein Prozess initialisiert eine Kommunikations Ressource mithilfe der [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) -Funktion erneut, die die folgenden Aufgaben ausführt:

-   Beendet ausstehende Lese-und Schreibvorgänge, auch wenn Sie noch nicht abgeschlossen wurden.
-   Verwirft ungelesene Zeichen und gibt die internen Ausgabe-und Eingabepuffer des Treibers frei, der der angegebenen Ressource zugeordnet ist.
-   Ordnet die internen Ausgabe-und Eingabepuffer neu zu.

Zum Aufrufen von [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)ist kein Prozess erforderlich. Wenn dies nicht der Fall ist, initialisiert der Treiber der Ressource das Gerät mit den Standardeinstellungen, wenn das Kommunikationsressourcen Handle zum ersten Mal verwendet wird.

 

 
