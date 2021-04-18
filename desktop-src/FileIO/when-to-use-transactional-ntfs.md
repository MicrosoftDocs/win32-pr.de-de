---
description: Verwenden Sie Transaktions-NTFS, um die Datenintegrität beizubehalten.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Verwendungszwecke von transaktionalen NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c0a134a8cb5824337022fedf14fe3db3c6f76c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347444"
---
# <a name="when-to-use-transactional-ntfs"></a>Verwendungszwecke von transaktionalen NTFS

Eine Anwendung kann Transaktions-NTFS (TxF) verwenden, um die Integrität der Daten auf dem Datenträger während unerwarteter Fehlerbedingungen beizubehalten. Im Allgemeinen sollte eine Anwendung TxF verwenden, wenn die Anwendung Dateien geleert und andere Techniken verwendet, um die Datenintegrität beizubehalten. TxF kann eine bessere Leistung erzielen und den Fehler Behandlungs Code der Anwendung vereinfachen und gleichzeitig die Fehlerwiederherstellung und Zuverlässigkeit verbessern. Die folgenden Abschnitte in diesem Thema enthalten Beispiele für Szenarien, in denen Sie TxF verwenden können.

## <a name="updating-a-file"></a>Aktualisieren einer Datei

Die Aktualisierung einer Datei ist ein gängiger und in der Regel einfacher Vorgang. Wenn das System oder die Anwendung jedoch fehlschlägt, während eine Anwendung Informationen auf einem Datenträger aktualisiert, kann das Ergebnis schwerwiegend sein, da die Benutzerdaten durch einen teilweise abgeschlossenen Datei Update Vorgang beschädigt werden können. Robuste Anwendungen führen oft komplexe Sequenzen von Datei Kopien und Dateinamen aus, um sicherzustellen, dass die Daten bei einem Systemausfall nicht beschädigt werden.

TxF vereinfacht es einer Anwendung, Datei Aktualisierungs Vorgänge vor System-oder Anwendungsfehlern zu schützen. Um eine Datei sicher zu aktualisieren, öffnet die Anwendung die Datei im transaktiven Modus, nimmt die erforderlichen Updates vor und führt einen Commit für die Transaktion aus. Wenn das System oder die Anwendung während des Datei Updates fehlschlägt, wird die Datei von TxF automatisch in dem Zustand wieder hergestellt, der vor dem Start der Datei aufgetreten ist. Dadurch wird die Beschädigung von Dateien vermieden.

## <a name="multi-file-updates"></a>Updates mit mehreren Dateien

TxF ist noch wichtiger, wenn sich ein einzelner logischer Vorgang auf mehrere Dateien auswirkt. Wenn Sie z. b. ein Tool zum Umbenennen einer der HTML-oder ASP-Seiten auf einer Website verwenden möchten, würde ein gut konzipiertes Tool auch alle Links so korrigieren, dass der neue Dateiname verwendet wird. Bei einem Fehler während dieses Vorgangs wird die Website jedoch in einem inkonsistenten Zustand belassen, und einige der Links verweisen immer noch auf den alten Dateinamen. Wenn Sie den Vorgang zum Umbenennen der Datei und den Link zur Korrektur einer einzelnen Transaktion vornehmen, stellt TxF sicher, dass die Datei umbenennen und die Link Korrektur als einzelner Vorgang erfolgreich ausgeführt werden kann oder fehlschlagen.

## <a name="consistent-concurrent-updates"></a>Konsistente gleichzeitige Updates

TxF isoliert gleichzeitige Transaktionen. Wenn eine Anwendung eine Datei für einen transaktionalen Lesevorgang öffnet, während eine andere Anwendung dieselbe Datei für eine transaktionale Aktualisierung geöffnet hat, isoliert TxF die Auswirkungen der beiden Transaktionen voneinander. Das heißt, dass der Transaktions Leser immer eine einzelne, konsistente Version der Datei anzeigt, auch wenn diese Datei gerade durch eine andere Transaktion aktualisiert wird.

Eine Anwendung kann diese Funktion verwenden, um es Kunden zu ermöglichen, Dateien anzuzeigen, während andere Kunden Updates vornehmen. Ein transaktionaler Webserver kann z. b. eine einheitliche Ansicht von Dateien bereitstellen, während ein anderes Tool diese Dateien gleichzeitig aktualisiert.

> [!Note]  
> TxF unterstützt keine gleichzeitigen Aktualisierungen durch mehrere Writer in unterschiedlichen Transaktionen. TxF unterstützt nur einen einzigen Writer mit mehreren gleichzeitigen und konsistenten Lesern.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Koordinieren mit anderen transaktiven Ressourcen-Managern

Transaktionen, die mit transaktiven Dateisystemen verwendet werden, können auch mit der transaktiven Registrierung verwendet werden. Updates für die Datei und die Registrierung werden mit einer einzelnen Transaktion koordiniert.

Mithilfe von [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC)-Transaktionen oder System. Transactions können Updates an SQL, MSMQ und anderen Transaktions Ressourcen mit transaktiven Datei Aktualisierungen koordiniert werden. Weitere Informationen finden Sie unter DTC es [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85)).

## <a name="unsupported-scenarios"></a>Nicht unterstützte Szenarien

TxF bietet keine Unterstützung für die folgenden Transaktions Szenarien:

-   Transaktionen auf Netzwerkvolumes, z. b. in Dateifreigaben. TxF wird von den CIFS/SMB-Protokollen nicht unterstützt.
-   Transaktionen in anderen Dateisystemen als NTFS.
-   Transaktive Vorgänge für Dateien, die durch Client seitiges zwischenspeichern zwischengespeichert werden.
-   Dateizugriff mithilfe von Objekt-IDs.
-   Alle freigegebenen Writer-Szenarios.
-   Jede Situation, in der eine Datei für einen längeren Zeitraum (Tage oder Wochen) geöffnet wird.

 

 
