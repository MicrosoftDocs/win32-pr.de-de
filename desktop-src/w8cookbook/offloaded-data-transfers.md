---
title: Offloaded-Datenübertragungen
description: Offloaded-Datenübertragungen
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- Auslagerung kopieren
- Auslagerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106337473"
---
# <a name="offloaded-data-transfers"></a>Offloaded-Datenübertragungen

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Um die Verschiebung der Speicherdaten voranzutreiben, hat Microsoft eine neue Datenübertragungstechnologie – offloaded Data Transfer (ODX) entwickelt. Anstelle von gepufferten Lese-und gepufferten Schreibvorgängen startet Windows ODX den Kopiervorgang mit einer Auslagerungs Überprüfung und ruft ein Token ab, das die Daten aus dem Speichergerät darstellt. Anschließend wird ein Auslagerungs Schreibbefehl mit dem Token verwendet, um die Daten Verschiebung vom Quell Datenträger zum Ziel Datenträger anzufordern. Der Kopier-Manager der Speichergeräte führt die Daten Verschiebung gemäß dem Token aus. In Windows 8 können der IT-Manager und der Speicher Administrator die Windows ODX-Funktion verwenden, um mit dem Speichergerät zu interagieren, um große Dateien oder Daten über das Hochgeschwindigkeitsspeicher Netzwerk zu verschieben. Windows ODX reduziert den Netzwerk Datenverkehr für Client Server und die CPU-Zeit Auslastung bei großen Datenübertragungen erheblich, da sich alle Daten Verschiebungen im Back-End-Speicher Netzwerk befinden. ODX kann bei der Bereitstellung virtueller Maschinen, bei der umfangreichen Datenmigration und bei der Unterstützung von mehrstufigen Speichergeräten verwendet werden. Zudem können die Kosten der physischen Hardware Bereitstellung durch die ODX-und Thin Bereitstellung-Speicher Features gesenkt werden.

> [!Note]  
> Diese Funktion kann nur auf Speichergeräten mit der Implementierung der SPC4-und SBC3-Spezifikation verwendet werden.

 

## <a name="functional-details"></a>Funktions Details

-   Das Windows ODX-Feature ist in die Kopier-Engine des Windows-Betriebssystems eingebettet. während der Speicherenumeration fragt Windows die ODX-Funktion des Speichergeräts ab.
-   Kopieren des Quell Speichergeräts und Kopieren des Zielspeicher Geräts sollten unter dem gleichen Kopier-Manager für die Unterstützung der Kopier Auslagerung verwaltet werden.
-   Wenn ein Kopiervorgang fehlschlägt, muss der Kopier-Manager des Speichergeräts die richtigen zusätzlichen Sense-Daten für die Fehlerbehandlung der APP zurückgeben.
-   Das Windows-Kopiermodul greift auf den herkömmlichen Kopiervorgang zurück, wenn der Kopiervorgang nicht ausgeführt werden kann.

## <a name="using-odx"></a>Verwenden von ODX

-   Die Datenübertragungs-app muss sicherstellen, dass sowohl Quell-als auch Kopier Ziel-LUN ODX-fähig sind, bevor die ODX-API-Routinen aufgerufen werden.
-   In Windows-Explorer können Benutzer "Drag" oder "Kopieren und Einfügen" verwenden, um die Kopier Auslagerung auszuführen.
-   Wenn die Quell-LUN und die Ziel-LUN mit dem Dateisystem bereitgestellt werden, muss die app nur FSCTL \_ Offload \_ Lesen und FSCTL \_ Offload- \_ Schreibvorgänge für die Datenübertragung von der Quell-LUN an die Ziel-LUN ausführen.
-   Wenn ein Kopiervorgang fehlschlägt, muss der Kopier-Manager des Speichergeräts die richtigen zusätzlichen Sense-Daten für die Fehlerbehandlung von apps zurückgeben.
-   Wenn die LUN der Quell-oder Ziel-LUN nicht mit dem Dateisystem bereitgestellt und gesperrt ist, muss die APP IOCTL \_ Storage- \_ \_ Daten \_ Satz \_ Attribute mit devicedsmaction \_ offloadread oder devicedsmaction \_ offloadwrite-Aktion zum Ausführen der Kopier Auslagerung abrufen.
-   Speicher Verwaltungs-Apps können eine SCSI- \_ Pass- \_ through-API verwenden, um offloaded-Datenübertragungen auszuführen, wenn sowohl die Quell-als auch die Ziel-LUNs nicht in einem Dateisystem eingebunden

## <a name="tests"></a>Tests

-   Überprüfen Sie die Windows ODX-Zertifizierung des Speicherarrays, um eine robuste Benutzer Leistung sicherzustellen.
-   Das Speichergerät muss die Zertifizierungsanforderungen für Windows offloaded Data Transfers (verwendet als Logo) erfüllen, um die ODX-Funktion zu unterstützen.
-   Verwenden Sie das Hardware zertifizierungskit für Windows offloaded Data Transfers, um die Unterstützung von ODX-Features für die Speichergeräte

## <a name="resources"></a>Ressourcen

-   T10 xcopy Lite spec (11-059r8)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [Hardware-Dashboard-Dienste](/windows-hardware/drivers/dashboard/)
-   [SCSI- \_ Durchlauf \_ Struktur](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 