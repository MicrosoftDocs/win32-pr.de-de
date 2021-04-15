---
title: Bewährte Methoden (Windows-Filter Plattform)
description: In der folgenden Liste finden Sie bewährte Methoden für die Entwicklung von Anwendungen mithilfe der Windows-Filter Plattform (WFP)-API.
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517288"
---
# <a name="best-practices-windows-filtering-platform"></a>Bewährte Methoden (Windows-Filter Plattform)

In der folgenden Liste finden Sie bewährte Methoden für die Entwicklung von Anwendungen mithilfe der Windows-Filter Plattform (WFP)-API.

-   Dynamische Sitzungen verwenden.

    Viele Anwendungen fügen beim Start Filter Richtlinien Objekte hinzu und löschen diese Objekte dann beim Ende. Durch die Verwendung einer dynamischen Sitzung garantieren Sie, dass diese Objekte auch dann gelöscht werden, wenn die Anwendung abstürzt. Außerdem ist das einfache Schließen des Engine-Handles am Ende effizienter, als einzelne Aufrufe zum Löschen der einzelnen Objekte zu erstellen.

-   Behandeln Sie Transaktions Timeouts ordnungsgemäß, oder legen Sie die Sitzungs- **txnwaittimeoutinmsec** auf unendlich fest, um Timeouts zu verhindern.

    Auch wenn Sie keine expliziten Transaktionen verwenden, werden die meisten Aufrufe weiterhin unter einer impliziten Transaktion ausgeführt, sodass ein Timeout möglich ist.

-   Verwenden Sie explizite Transaktionen, um verwandte Add-oder DELETE-Vorgänge in einer einzelnen Transaktion zu kombinieren.

    Dies ist effizienter und erleichtert das Bereinigen von partiellen Ergebnissen in Fehler Pfaden.

-   Verwenden Sie MUI-kompatible Zeichen folgen.

    Alle lokalisierbaren Zeichen folgen werden in einer gemeinsamen Datenstruktur gespeichert: [**swpm- \_ Anzeige \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Die Zeichen folgen in dieser Struktur können indirekte Zeichen Folgen des Typs sein, der von [**shloadderetstring**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)unterstützt wird. Bevor eine **fwpm- \_ Anzeige \_ DATA0** -Struktur von einer der Funktionen zurückgegeben wird, werden die indirekten Zeichen folgen mithilfe des Gebiets Schemas des Aufrufers in die angegebene Zeichen folgen Ressource aufgelöst.

-   Ordnen Sie alle Objekte einem Anbieter zu.

    Wenn mehrere Anbieter auf dem System installiert sind, ist es für Diagnosetools einfacher, festzustellen, wer was hinzugefügt hat.

-   Fügen Sie Ihrer eigenen Unterschicht Filter hinzu.

    Sobald ein Beendender Filter in einer untergeordneten Ebene gedrückt wird, werden keine weiteren Filter in dieser Unterschicht ausgewertet. Wenn Sie also die Filter der gleichen Unterschicht wie ein anderer Anbieter hinzufügen, können Sie verhindern, dass die Filter des anderen aufgerufen werden, was zu unerwarteten Ergebnissen führt.

-   Verwenden Sie anstelle der Paket orientierten Filterung die Anwendungsschicht-Erzwingung (ALE).

    Das Filtern auf Paketebene ist langsam.

-   Filtern Sie ICMP-Fehler und RST-Ereignisse, bevor Sie generiert werden.

    Dies ist effizienter, wenn diese Ereignisse gefiltert werden, nachdem Sie generiert wurden.

-   Führen Sie die Paketüberprüfung in der Stream/Datagramm-Datenschicht statt auf der Transport Ebene durch.

    Dies gilt für die Entwicklung von Legenden. Weitere Informationen finden Sie unter [Überlegungen zur Programmierung von Legenden Treibern](/windows-hardware/drivers/network/callout-driver-programming-considerations) im Windows-Treiberkit (WDK).

-   Beachten Sie bei der Verwendung komplexer Filter Auswirkungen auf die Leistung.

    Ab Windows 7 und Windows Server 2008 R2 können Filter mit mehreren Bedingungen erstellt werden, die denselben Feld Schlüssel verwenden. Dadurch können komplexe Richtlinien mit weniger Filtern erstellt werden. Solche komplexen Filter können jedoch eine langsamere Leistung verursachen, damit das WFP-Filtermodul klassifiziert werden kann. Es sollte eine Auswertung vorgenommen werden, um zu bestimmen, ob die Verwendung solcher Filter eine negative Auswirkung auf die Gesamtleistung der Lösung verursacht.

 

 
