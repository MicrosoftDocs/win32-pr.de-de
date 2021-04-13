---
title: Multipfad-e/a unterstützt jetzt erweiterte Speicher Anforderungs Blöcke.
description: Multipfad-e/a unterstützt jetzt erweiterte Speicher Anforderungs Blöcke.
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104316658"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>Multipfad-e/a unterstützt jetzt erweiterte Speicher Anforderungs Blöcke.

## <a name="platforms"></a>Plattformen

**Server** – Windows Server 2012 

## <a name="description"></a>BESCHREIBUNG

In Windows Server 2012, einer neuen Struktur, ersetzt der Speicher \_ Anforderungs \_ Block (Extended SRB) den SCSI- \_ Anforderungs \_ Block (Legacy SRB) im Kernspeicher Stapel. Erweiterte SRSB repliziert die Funktionalität der Legacy-SRSB, sind aber auch erweiterbar und skalierbar.

Multipfad-e/a (MPIO) unterstützt erweiterte SRSB und ermöglicht es gerätespezifischen Modulen (DSMs), auch erweiterte SRB-Unterstützung anzugeben. Damit der Speicher Stapel eines Multipfad-Geräts erweiterte SRB-Objekte verwenden kann, **müssen jedoch alle Komponenten im Stapel erweiterte SRB-Unterstützung (einschließlich DSM) unterstützen**. Beachten Sie, dass das Microsoft-in-Box-DSM, MSDSM, erweiterte SRSB unterstützt.

Die SCSI- \_ Pass- \_ through- \_ Struktur ist nicht Teil der erweiterten MPIO-Pass-Through-Struktur, da der erweiterte SCSI-Durchlauf eine Variable Größe aufweisen kann, je nach Befehlszeilen Debugger (CDB). Stattdessen verfügt der erweiterte MPIO-Durchlauf über ein Feld, das den Offset vom Anfang der erweiterten MPIO-Pass-Through-Struktur zur SCSI- \_ Pass-Through-Struktur beschreibt \_ \_ . Der Aufrufer muss sicherstellen, dass er einen Puffer der entsprechenden Größe zuweist und den SCSI-Pass-Through-Offset ordnungsgemäß festgelegt Solange der Aufrufer den Regeln für erweiterte SCSI-Pass-Through-Vorgänge folgt, sollten keine zusätzlichen Aufgaben für die Verwendung des erweiterten MPIO-Pass-Through ausgeführt werden.

> [!Note]  
> Wenn das DSM erweiterte SRB nicht unterstützt, schlägt MPIO für erweiterte MPIO-Pass-Through-Anforderungen fehl, für die das MPIO \_ IOCTL- \_ Flag das \_ DSM- \_ Flag Set umfasst.

 

## <a name="manifestation"></a>Ausstrahlung

Wenn ein beliebiger Teil des Speicher Stapels des Geräts, einschließlich DSM, erweiterte SRB-Objekte nicht unterstützt, wird der Speicher Stapel auf Legacy-SRB zurückgesetzt.

## <a name="solution"></a>Lösung

Es gibt nur zwei MPIO-Anforderungen für ein DSM, um Speicher Anforderungs Blöcke zu unterstützen \_ \_ :

-   Das DSM muss seinen Typ als DsmType6 melden.
-   Das DSM muss die Funktion "DSM \_ Address \_ Type \_ supported" bereitstellen.

Wenn das DSM DsmType6 nicht meldet oder wenn es meldet DsmType6, aber die Funktion "DSM Address Type supported" nicht bereitstellt \_ \_ \_ , wird von MPIO angenommen, dass das DSM erweiterte SRSB nicht unterstützt.

Die \_ \_ unterstützte DSM Address Type- \_ Funktion akzeptiert zwei Parameter, von denen einer ein Adresstyp ist. Dieser Adresstyp muss einer der Werte für den Speicher \_ \_ Adresstyp sein, der \_ \* in SRB. h definiert ist. Das DSM muss "true" zurückgeben, wenn es den angegebenen adrestyp unterstützt, andernfalls "false". Die Definition von "Support" ist letztendlich das DSM. MPIO verwendet diese Funktion, um sicherzustellen, dass das DSM nicht falsch verhält, wenn ein erweitertes SRB mit einer Stor- \_ Adressstruktur des angegebenen Typs übergeben wird. Daher ruft MPIO diese Funktion im Allgemeinen auf, wenn ein multipfadgerät aufgezählt wird, aber die Funktion kann jederzeit aufgerufen werden.

Wenn ein DSM nie die Stor-Adresse eines erweiterten SRB berührt \_ , kann es für jeden gültigen Wert des Speicher \_ Adress Typs "true" zurückgeben \_ \_ \* . Lesen Sie das Beispiel-DSM im WDK.

**Andere wichtige Hinweise**

-   DSMs, die erweiterte SRBs unterstützen, muss sowohl SCSI \_ -Anforderungs \_ Block Strukturen als auch Speicher \_ Anforderungs Block- \_ Strukturen verarbeiten können. Nur weil ein DSM meldet, dass erweiterte SRSB unterstützt werden, bedeutet das nicht, dass es exklusiv erweiterte SRSB empfängt. Es kann weiterhin eine beliebige Anzahl von Legacy-SRB-Systemen zusätzlich zu erweiterten SRB-Systemen empfangen und muss daher beide verarbeiten können.
-   Wir haben im WDK eine Header Datei mit dem Namen "srbhelper. h" bereitgestellt, die Inline Funktionen enthält, um Treiber zu unterstützen, die sowohl erweiterte als auch ältere SRB verarbeiten müssen. In unserem Beispiel-DSM wird dieser Header verwendet, damit Sie ihn als ein Beispiel für die Verwendung dieser Funktionen verwenden können.
-   Ein DSM, das erweiterte SRSB nicht unterstützt, muss niemals erweiterte SRSB verarbeiten.
-   Es ist möglich, dass ein MPIO dazu führt, dass der Speicher Stapel auf Legacy-SRB zurückgreift, wenn das DSM einen bestimmten Speicher Adresstyp nicht unterstützt \_ \_ \_ \* (aber andernfalls erweiterte SRB unterstützt).
-   "BTL8" ist der einzige Speicher \_ Adresstyp, der \_ \_ \* derzeit für Windows Server 2012 definiert ist.

 

 




