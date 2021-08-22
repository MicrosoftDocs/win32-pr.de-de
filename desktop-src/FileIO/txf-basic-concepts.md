---
description: Beschreibt Die Konzepte für Read Committed-Konsistenz, Read Committed-Isolation und Transaktionssperren in Transaktional NTFS.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Grundlegende TxF-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71b2ed4e906fab881fac93a686dcf3aff6e8a95fa72d785ef14320ef92c05ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950969"
---
# <a name="basic-txf-concepts"></a>Grundlegende TxF-Konzepte

## <a name="read-isolation"></a>Leseisolation

Transaktionales NTFS (TxF) bietet Konsistenz mit Read Committed.

Ein [*transaktiver Writer*](glossary.md) bezieht sich auf ein transaktives Dateihandles, das mit jeder Berechtigung geöffnet wird, die nicht Teil des generischen Lesezugriffs, sondern Teil des generischen Schreibzugriffs ist. Ein *transaktiver Writer* sieht die neueste Version einer Datei, die alle Änderungen derselben Transaktion enthält. Pro Datei kann nur ein transaktiver Writer verwendet werden. Nicht transaktive Writer werden immer von einem transaktiven Writer blockiert, auch wenn die Datei mit freigegebenen Schreibberechtigungen geöffnet wird.

Ein [*transaktiver Reader*](glossary.md) bezieht sich auf ein transaktives Dateihandles, das mit jeder Berechtigung geöffnet wird, die Teil des generischen Lesezugriffs, aber nicht Teil des generischen Schreibzugriffs ist. Ein *transaktiver Reader* sieht eine Version der Datei, für die ein Committed durchgeführt wurde, die zum Zeitpunkt des Öffnens des Dateihandles vorhanden war. Der transaktive Reader ist von den Auswirkungen von transaktiven Writern isoliert. Dies bietet eine konsistente Ansicht der Datei nur für die Lebensdauer des Dateihandpunkts und blockiert nicht transaktive Writer.

> [!Note]  
> Wenn ein Handle für die Änderung mit der [**CreateFileTransacted-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) geöffnet wurde, werden alle nachfolgenden Öffnen der Datei innerhalb dieser Transaktion , unabhängig davon, ob sie schreibgeschützt sind oder nicht, vom System zu isolations- und anderen Transaktionssemantikzwecken in einen transaktiven Writer konvertiert. Dies bedeutet, dass das Handle in der Folge, wenn ein Handle für den schreibgeschützten Zugriff geöffnet wird, vor dem Start der Transaktion keine Ansicht der Datei erhält. er empfängt die aktive Transaktionsansicht der Datei.

 

Ein nicht transaktives Dateihandl sieht keine Änderungen, die innerhalb einer Transaktion vorgenommen wurden, bis für die Transaktion ein Committed ausgeführt wurde. Das nicht transaktive Dateihandles empfängt eine isolierte Sicht, die einem transaktiven Reader ähnelt. Im Gegensatz zu einem transaktiven Reader empfängt es jedoch das Dateiupdate, wenn ein transaktiver Writer einen Commit für die Transaktion ausgeführt hat.

## <a name="isolation-levels"></a>Isolationsstufen

TxF bietet Read Committed-Isolation. Dies bedeutet, dass Dateiupdates außerhalb der Transaktion nicht angezeigt werden. Wenn eine Datei beim Lesen von Dateien innerhalb der Transaktion mehr als einmal geöffnet wird, werden bei jedem nachfolgenden Öffnen möglicherweise unterschiedliche Ergebnisse angezeigt. Dateien, die beim ersten Zugriff verfügbar waren, sind möglicherweise nicht verfügbar (weil sie gelöscht wurden) oder umgekehrt.

## <a name="transactional-locking"></a>Transaktionssperren

Durch das Erstellen eines transaktiven Writers für eine *Datei wird die Datei* transaktional gesperrt. Nachdem eine Datei durch eine Transaktion gesperrt wurde, tritt bei anderen Dateisystemvorgängen außerhalb der Sperrentransaktion, die versuchen, die transaktionsgesperrte Datei zu ändern, ein Fehler auf, der entweder mit **ERROR \_ SHARING \_ VIOLATION** oder **ERROR \_ TRANSACTIONAL CONFLICT \_ auftritt.**

In der folgenden Tabelle werden die Transaktionssperren zusammengefasst.



Datei, die derzeit von geöffnet wird

Datei geöffnet, die von versucht wurde

Transacted

Nicht transaktiv

Leser

Reader/Writer

Leser

Reader/Writer

Transaktiver Reader

Ja

Ja

Ja

Nein 2

Transaktiver Reader/Writer

Ja

Nein 2

Ja

Nein 2

Nicht transaktiver Reader

Ja

Ja

Ja

Ja

Nicht transaktiver Reader/Writer

Nein

Nein

Ja

Ja

1. Fehler mit **ERROR \_ TRANSACTIONAL \_ CONFLICT**<br/> 2. Fehler bei **\_ \_ FEHLERFREIGABEVERLETZUNG**<br/>



 

Wenn Sie einen benannten Stream für eine Änderung öffnen, die eine Transaktion verwendet, muss die gesamte Datei gesperrt werden.

Neben transaktionsbasierten Sperren gelten typische NTFS-Dateifreigaberegeln.

Sie müssen die folgenden beiden Dateifreigabemodi parallel berücksichtigen:

-   Der Transaktionssperrmodus.
-   Normale Dateifreigabemodi.

Welcher Modus restriktiver ist, ist der, der angewendet wird.

 

 




