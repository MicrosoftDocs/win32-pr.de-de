---
description: Beschreibt die Konsistenz mit Lese-und Schreibzugriff, die Isolation mit Lese-und Schreibzugriff sowie die Konzepte von Transaktions Sperren in Transaktions-NTFS.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Grundlegende TxF-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347819"
---
# <a name="basic-txf-concepts"></a>Grundlegende TxF-Konzepte

## <a name="read-isolation"></a>Lese Isolation

Transaktionale NTFS (TxF) bieten Konsistenz mit Lesezugriff.

Ein [*transaktiver Writer*](glossary.md) verweist auf ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet wurde, die nicht Teil des generischen Lese Zugriffs ist, aber Teil des generischen Schreibzugriffs ist. Ein *transaktiver Writer* zeigt die neueste Version einer Datei an, die alle Änderungen durch dieselbe Transaktion enthält. Pro Datei kann nur ein transaktiver Writer vorhanden sein. Nicht transaktive Writer werden immer von einem transaktiven Writer blockiert, auch wenn die Datei mit freigegebenen Schreibberechtigungen geöffnet ist.

Ein [*transaktiver Reader*](glossary.md) verweist auf ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet ist, die Teil des generischen Lese Zugriffs ist, aber nicht Teil des generischen Schreibzugriffs ist. Ein *transaktiver Reader* zeigt eine zugesicherte Version der Datei an, die zum Zeitpunkt des Öffnens des Datei Handles vorhanden war. Der transaktive Reader ist von den Auswirkungen von transaktiven Writern isoliert. Dies bietet eine konsistente Ansicht der Datei nur für die Lebensdauer des Datei Handles und blockiert nicht transaktive Writer.

> [!Note]  
> Wenn ein Handle für die Änderung mit der Funktion " [**fiatefiletransfailed**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) " geöffnet wurde, werden alle nachfolgenden Dateien innerhalb dieser Transaktion, unabhängig davon, ob schreibgeschützt oder nicht, vom System in einen transaktiven Writer konvertiert, um die Isolation und andere Transaktions Semantik zu untersuchen. Dies bedeutet Folgendes: Wenn ein Handle für den schreibgeschützten Zugriff geöffnet wird, empfängt das Handle vor dem Start der Transaktion keine Ansicht der Datei. Er empfängt die aktive Transaktions Ansicht der Datei.

 

Bei einem nicht transaktiven Datei Handle werden innerhalb einer Transaktion vorgenommene Änderungen erst angezeigt, wenn für die Transaktion ein Commit ausgeführt wurde. Das nicht transaktive Datei Handle empfängt eine isolierte Ansicht, die einem transaktiven Reader ähnelt, aber im Gegensatz zu einem transaktiven Reader empfängt er das Datei Update, wenn ein transaktiver Writer einen Commit für die Transaktion ausführt.

## <a name="isolation-levels"></a>Isolationsstufen

TxF bietet eine Isolation mit Lesezugriff. Dies bedeutet, dass Datei Updates außerhalb der Transaktion nicht sichtbar sind. Wenn eine Datei beim Lesen von Dateien innerhalb der Transaktion mehrmals geöffnet wird, werden möglicherweise unterschiedliche Ergebnisse angezeigt. Dateien, die beim ersten Zugriff verfügbar waren, sind möglicherweise nicht verfügbar (weil Sie gelöscht wurden) oder umgekehrt.

## <a name="transactional-locking"></a>Transaktionale Sperren

Wenn Sie einen transaktiven Writer in einer Datei erstellen, wird die Datei in *transaktional* gesperrt. Nachdem eine Datei durch eine Transaktion gesperrt wurde, treten bei anderen Dateisystem Vorgängen außerhalb der Sperr Transaktion, die versuchen, die im Transaktionsmodus gesperrte Datei zu ändern, entweder **Fehler \_ Freigabe \_ Verletzungen** oder **Fehler \_ Transaktions \_ Konflikte** auf.

In der folgenden Tabelle wird die Transaktions Sperre zusammengefasst.



Zurzeit geöffnete Datei

Datei öffnen versucht von

Transacted

Nicht transaktiv

Leser

Leser/Writer

Leser

Leser/Writer

Transaktive Reader

Ja

Ja

Ja

Nein 2

Transaktive Reader/Writer

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

1. Schlägt mit **\_ fehlerellem Transaktions \_ Konflikt** fehl<br/> 2. Fehler bei **der \_ Freigabe \_ Verletzung**<br/>



 

Wenn Sie einen benannten Stream für eine Änderung öffnen, die eine Transaktion verwendet, muss die gesamte Datei gesperrt werden.

Zusätzlich zum Transaktions Sperren gelten typische NTFS-Regeln für die Dateifreigabe.

Sie müssen die folgenden beiden Dateifreigabe Modi parallel in Erwägung gezogen werden:

-   Der Modus für die transaktionale Sperrung.
-   Normaler Modus für die Dateifreigabe.

Welcher Modus restriktiver ist, ist der, der angewendet wird.

 

 




