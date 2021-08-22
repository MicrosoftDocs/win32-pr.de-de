---
title: Bewährte Methoden (Windows Filterplattform)
description: Die folgende Liste enthält bewährte Methoden zum Entwickeln von Anwendungen mithilfe der WFP-API (Windows Filtering Platform).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ddb6038a9fe43070f1c16e545dbd7ac8929f3363fc88556aac391428175ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069460"
---
# <a name="best-practices-windows-filtering-platform"></a>Bewährte Methoden (Windows Filterplattform)

Die folgende Liste enthält bewährte Methoden zum Entwickeln von Anwendungen mithilfe der WFP-API (Windows Filtering Platform).

-   Verwenden sie dynamische Sitzungen.

    Viele Anwendungen fügen beim Start Filterungsrichtlinienobjekte hinzu und löschen diese Objekte dann am Ende. Mithilfe einer dynamischen Sitzung garantieren Sie, dass diese Objekte gelöscht werden, auch wenn die Anwendung abstürzt. Darüber hinaus ist das einfache Schließen des Engine-Handles am Ende effizienter als einzelne Aufrufe zum Löschen der einzelnen Objekte.

-   Behandeln Sie Transaktionstimeouts ordnungsgemäß, oder legen Sie die Sitzung **txnWaitTimeoutInMSec** auf unendlich fest, um Timeouts zu verhindern.

    Auch wenn Sie keine expliziten Transaktionen verwenden, werden die meisten Aufrufe weiterhin unter einer impliziten Transaktion ausgeführt und können daher ein Timeout erreichen.

-   Verwenden Sie explizite Transaktionen, um verknüpfte Add- oder Delete-Vorgänge in einer einzelnen Transaktion zu kombinieren.

    Dies ist effizienter und erleichtert das Bereinigen von Teilergebnissen in Fehlerpfaden.

-   Verwenden Sie DIE RICHTLINIENkonformen Zeichenfolgen.

    Alle lokalisierbaren Zeichenfolgen werden in einer gemeinsamen Datenstruktur gespeichert: [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Die Zeichenfolgen in dieser Struktur können indirekte Zeichenfolgen des Typs sein, der von [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)unterstützt wird. Bevor eine **FWPM \_ DISPLAY \_ DATA0-Struktur** von einer der Funktionen zurückgegeben wird, werden die indirekten Zeichenfolgen mithilfe des Gebietsschemas des Aufrufers in die angegebene Zeichenfolgenressource aufgelöst.

-   Ordnen Sie einem Anbieter alle Objekte zu.

    Wenn mehrere Anbieter auf dem System installiert sind, ist es für Diagnosetools einfacher zu bestimmen, wer was hinzugefügt hat.

-   Fügen Sie Ihrer eigenen Unterschicht Filter hinzu.

    Sobald ein abschließender Filter in einer Unterebene erreicht wurde, werden keine filter mehr in dieser Unterschicht ausgewertet. Wenn Sie also Ihre Filter derselben Unterebene wie ein anderer Anbieter hinzufügen, können Sie verhindern, dass die Filter des jeweils anderen Anbieters aufgerufen werden, was zu unerwarteten Ergebnissen führt.

-   Verwenden Sie Application Layer Enforcement (ALE) anstelle der paketorientierten Filterung.

    Die Filterung auf Paketebene ist langsam.

-   Filtern Sie ICMP-Fehler und RST-Ereignisse, bevor sie generiert werden.

    Dies ist effizienter als das Filtern dieser Ereignisse nach deren Generierung.

-   Führen Sie die Paketuntersuchung auf Der Stream-/Datagram-Datenebene und nicht auf der Transportebene durch.

    Dies gilt für die Entwicklung von Callouts. Weitere Informationen finden Sie unter Überlegungen zur Programmierung von [Callouttreibern](/windows-hardware/drivers/network/callout-driver-programming-considerations) im Windows Driver Kit (WDK).

-   Berücksichtigen Sie Leistungsauswirkungen bei der Verwendung komplexer Filter.

    Ab Windows 7 und Windows Server 2008 R2 können Filter mit mehreren Bedingungen erstellt werden, die denselben Feldschlüssel verwenden. Dadurch können komplexe Richtlinien mit weniger Filtern erstellt werden. Solche komplexen Filter können jedoch eine langsamere Leistung für die Klassifizierung der WFP-Filter-Engine verursachen. Es sollte eine Auswertung durchgeführt werden, um zu bestimmen, ob die Verwendung solcher Filter negative Auswirkungen auf die Gesamtleistung Ihrer Lösung hat.

 

 
