---
title: Multipfad-E/A unterstützt jetzt erweiterte Speicheranforderungsblöcke.
description: Multipfad-E/A unterstützt jetzt erweiterte Speicheranforderungsblöcke.
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b3a5ce3050bf7fddc2bd77da30e766c7b9cd67a8c4f49c753da5302b104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932210"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>Multipfad-E/A unterstützt jetzt erweiterte Speicheranforderungsblöcke.

## <a name="platforms"></a>Plattformen

**Server** – Windows Server 2012 

## <a name="description"></a>Beschreibung

In Windows Server 2012, einer neuen Struktur, ersetzt STORAGE \_ REQUEST \_ BLOCK (erweiterter SRB) den SCSI \_ REQUEST BLOCK \_ (Legacy-SRB) im Kernspeicherstapel. Erweiterte SRBs replizieren die Funktionalität der Legacy-SRBs, sind aber auch erweiterbar und skalierbar.

Multipfad-E/A (MPIO) unterstützt erweiterte SRBs und ermöglicht es Gerätespezifischen Modulen (DSMs), auch erweiterte SRB-Unterstützung anzugeben. Damit der Speicherstapel eines Multipfadgeräts erweiterte SRBs verwenden kann, müssen jedoch alle Komponenten im Stapel erweiterte **SRBs unterstützen, einschließlich DSM**. Beachten Sie, dass das microsoft-in-box-DSM MSDSM erweiterte SRBs unterstützt.

Die SCSI PASS THROUGH EX-Struktur ist nicht Teil der erweiterten \_ \_ MPIO-Pass-Through-Struktur, da der erweiterte SCSI-Pass-Through je nach Befehlszeilendebugger (CDB) eine variable Größe \_ haben kann. Stattdessen verfügt der erweiterte MPIO-Pass-Through über ein Feld, das den Offset vom Anfang der erweiterten MPIO-Pass-Through-Struktur zur \_ SCSI-PASS \_ THROUGH \_ EX-Struktur beschreibt. Der Aufrufer muss sicherstellen, dass er einen Puffer der entsprechenden Größe zuteilen und den SCSI-Pass-Through-Offset ordnungsgemäß festlegen. Solange der Aufrufer die Regeln für erweiterte SCSI-Pass-Throughs einfing, sollte es keine zusätzlichen Arbeit für ihn geben, um den erweiterten MPIO-Pass-Through zu verwenden.

> [!Note]  
> Wenn das DSM erweiterte SRBs nicht unterstützt, führt MPIO zu einem Fehler bei erweiterten MPIO-Pass-Through-Anforderungen, für die das \_ MPIO-IOCTL-FLAG \_ \_ INVOLVE \_ DSM festgelegt ist.

 

## <a name="manifestation"></a>Manifestation

Wenn ein Teil des Speicherstapels des Geräts, einschließlich DSM, keine erweiterten SRBs unterstützt, verwendet der Speicherstapel wieder ältere SRBs.

## <a name="solution"></a>Lösung

Es gibt nur zwei MPIO-Anforderungen für ein DSM zur Unterstützung von \_ STORAGE-ANFORDERUNGSBLÖCKEn: \_

-   Das DSM muss seinen Typ als DsmType6 melden.
-   Das DSM muss die DSM-Funktion \_ ADDRESS \_ TYPE SUPPORTED \_ bereitstellen.

Wenn das DSM DsmType6 nicht meldet oder DsmType6 meldet, aber nicht die DSM ADDRESS TYPE SUPPORTED-Funktion zur Verfügung stellt, geht MPIO davon aus, dass \_ \_ das DSM erweiterte SRBs nicht \_ unterstützt.

Die DSM \_ ADDRESS \_ TYPE \_ SUPPORTED-Funktion akzeptiert zwei Parameter, von denen einer ein Adresstyp ist. Dieser Adresstyp muss einer der in srb.h definierten STORAGE \_ ADDRESS \_ \_ \* TYPE-Werte sein. Das DSM muss TRUE zurückgeben, wenn es den angegebenen Adresstyp unterstützt, ander nicht FALSE. Die Definition von "Unterstützung" hängt letztendlich vom DSM ab. MPIO verwendet diese Funktion, um sicherzustellen, dass sich das DSM nicht falsch verhält, wenn ihm ein erweiterter SRB mit einer STOR ADDRESS-Struktur des angegebenen Typs \_ übergeben wird. Daher ruft MPIO diese Funktion im Allgemeinen auf, wenn ein Multipfadgerät aufzählt, aber die Funktion kann jederzeit aufgerufen werden.

Wenn ein DSM nie die STOR-ADRESSE eines erweiterten SRB berührt, kann es TRUE für jeden gültigen \_ \_ SPEICHERADRESSENTYP-Wert \_ \_ \* zurückgeben. Sehen Sie sich das Beispiel-DSM im WDK an.

**Weitere wichtige Hinweise**

-   DSMs, die erweiterte SRBs unterstützen, müssen sowohl SCSI REQUEST BLOCK-Strukturen als auch \_ \_ STORAGE REQUEST \_ \_ BLOCK-Strukturen verarbeiten können. Nur weil ein DSM meldet, dass es erweiterte SRBs unterstützt, bedeutet dies nicht, dass es ausschließlich erweiterte SRBs erhält. Sie kann zusätzlich zu erweiterten SRBs weiterhin eine beliebige Anzahl von Legacy-SRBs empfangen und muss daher in der Lage sein, beides zu verarbeiten.
-   Wir haben im WDK eine Headerdatei namens srbhelper.h bereitgestellt, die Inlinefunktionen enthält, die Treiber unterstützen, die sowohl erweiterte als auch ältere SRBs verarbeiten müssen. Unser Beispiel-DSM verwendet diesen Header, damit Sie ihn als Beispiel für die Verwendung dieser Funktionen verwenden können.
-   Ein DSM, das erweiterte SRBs nicht unterstützt, muss nie erweiterte SRBs verarbeiten.
-   Es ist möglich, dass ein MPIO dazu führt, dass der Speicherstapel auf ältere SRBs zurückfallt, wenn das DSM keinen bestimmten SPEICHERADRESSENTYP unterstützt (aber andernfalls erweiterte \_ \_ \_ \* SRBs unterstützt).
-   "BTL8" ist der einzige \_ \_ SPEICHERADRESSENTYP, \_ \* der derzeit für Windows Server 2012 definiert ist.

 

 




