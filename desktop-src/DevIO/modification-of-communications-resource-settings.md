---
description: Wenn die CreateFile-Funktion ein Handle für eine serielle Kommunikationsressource öffnet, initialisiert und konfiguriert das System die Ressource gemäß den Werten, die beim letzten Öffnen der Ressource eingerichtet wurden.
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: Änderung des Kommunikationsressourcen-Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a4658c58c07dfbd7ffe8ba7977db587211d3422359677999db312d05bd2c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911985"
---
# <a name="modification-of-communications-resource-settings"></a>Änderung des Kommunikationsressourcen-Einstellungen

Wenn die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ein Handle für eine serielle Kommunikationsressource öffnet, initialisiert und konfiguriert das System die Ressource gemäß den Werten, die beim letzten Öffnen der Ressource eingerichtet wurden. Wenn die vorherigen Einstellungen beibehalten werden, kann  der Benutzer die einstellungen beibehalten, die über einen Modusbefehl angegeben wurden, wenn das Gerät erneut geöffnet wird. Die vom vorherigen Geöffnetvorgang geerbten Werte umfassen die Konfigurationseinstellungen des Gerätesteuerungsblocks (eine [**DCB-Struktur)**](/windows/desktop/api/Winbase/ns-winbase-dcb) und die time out-Werte, die in E/A-Vorgängen verwendet werden. Wenn das Gerät noch nie geöffnet wurde, wird es mit den Standardeinstellungen des Systems konfiguriert.

Um die Erstkonfiguration einer seriellen Kommunikationsressource zu bestimmen, ruft ein Prozess die [**GetCommState-Funktion**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) auf, die eine [**DCB-Struktur**](/windows/desktop/api/Winbase/ns-winbase-dcb) des seriellen Anschlusses mit den aktuellen Konfigurationseinstellungen füllt. Um diese Konfiguration zu ändern, gibt ein Prozess eine **DCB-Struktur** in einem Aufruf der [**SetCommState-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) an.

Member der [**DCB-Struktur**](/windows/desktop/api/Winbase/ns-winbase-dcb) geben die Konfigurationseinstellungen an, z. B. die Baudrate, die Anzahl der Datenbits pro Byte und die Anzahl der Stoppbits pro Byte. Andere **DCB-Member** geben Sonderzeichen an und ermöglichen die Paritätsüberprüfung und Flusssteuerung. Wenn ein Prozess nur einige dieser Konfigurationseinstellungen ändern muss, sollte er zuerst [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) aufrufen, um eine **DCB-Struktur** mit der aktuellen Konfiguration zu füllen. Anschließend kann der Prozess die wichtigen Werte in der **DCB-Struktur** anpassen und das Gerät durch Aufrufen von [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) und Angeben der geänderten **DCB-Struktur neu** konfigurieren. Mit diesem Verfahren wird sichergestellt, dass die unveränderten Member der **DCB-Struktur** geeignete Werte enthalten. Ein häufiger Fehler ist beispielsweise das Konfigurieren eines Geräts mit einer **DCB-Struktur,** bei der das **XonChar-Member** der Struktur gleich dem **XoffChar-Member** ist.

Die [**Funktion BuildCommDCB bietet**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba) eine weitere Möglichkeit, eine [**DCB-Struktur zu**](/windows/desktop/api/Winbase/ns-winbase-dcb) ändern. **BuildCommDCB** verwendet eine Zeichenfolge in der gleichen Form  wie die Befehlszeilenargumente des Modusbefehls, um die Baudrate, das Paritätsschema, die Anzahl der Stoppbits und die Anzahl der Datenbits anzugeben. Die verbleibenden Member von [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) werden von dieser Funktion nicht geändert, außer dass die entsprechenden Member so festgelegt sind, dass XON/XOFF und die Hardwareflusssteuerung deaktiviert werden. **BuildCommDCB ändert** nur eine **DCB-Struktur.** Das Gerät wird nicht neu konfiguriert.

Ein Prozess kann eine Kommunikationsressource mithilfe der [**GetCommProperties-Funktion**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) neu konfigurieren, um Informationen von einem Gerätetreiber zu den unterstützten Konfigurationseinstellungen zu erhalten. Der Prozess kann diese Informationen verwenden, um zu vermeiden, dass eine Konfiguration angegeben wird, die nicht unterstützt wird.

Die [**SetCommState-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) konfiguriert die Kommunikationsressource neu, wirkt sich jedoch nicht auf die interne Ausgabe und die Eingabepuffer des angegebenen Treibers aus. Die Puffer werden nicht geleert, und ausstehende Lese- und Schreibvorgänge werden nicht vorzeitig beendet.

Ein Prozess initialisiert eine Kommunikationsressource erneut mithilfe der [**SetupComm-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) die die folgenden Aufgaben ausführt:

-   Beendet ausstehende Lese- und Schreibvorgänge, auch wenn sie nicht abgeschlossen wurden.
-   Verwirft ungelesene Zeichen und gibt die internen Ausgabe- und Eingabepuffer des Treibers frei, der der angegebenen Ressource zugeordnet ist.
-   Neuverlegung der internen Ausgabe- und Eingabepuffer.

Zum Aufrufen von [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)ist kein Prozess erforderlich. Falls nicht, initialisiert der Treiber der Ressource das Gerät bei der ersten Verwendung des Handles der Kommunikationsressource mit den Standardeinstellungen.

 

 
