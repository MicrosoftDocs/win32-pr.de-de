---
description: Verwenden Sie transaktionales NTFS, um die Datenintegrität aufrechtzuerhalten.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Wann sollte ntfs für Transaktionen verwendet werden?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f7a67fe6960a8754f768956457afbd04a509bbf9a3c18360b4651e4d9ccda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830130"
---
# <a name="when-to-use-transactional-ntfs"></a>Wann sollte ntfs für Transaktionen verwendet werden?

Eine Anwendung kann Transaktionales NTFS (TxF) verwenden, um die Integrität von Daten auf dem Datenträger bei unerwarteten Fehlerbedingungen beizubehalten. Im Allgemeinen sollte eine Anwendung die Verwendung von TxF in Betracht ziehen, wenn die Anwendung Dateien leert, und andere Techniken verwenden, um die Datenintegrität aufrechtzuerhalten. TxF kann eine bessere Leistung bieten und den Fehlerbehandlungscode der Anwendung vereinfachen und gleichzeitig die Fehlerwiederherstellung und -zuverlässigkeit verbessern. Die folgenden Abschnitte in diesem Thema enthalten Beispiele für Szenarien für die Verwendung von TxF.

## <a name="updating-a-file"></a>Aktualisieren einer Datei

Das Aktualisieren einer Datei ist ein gängiger und in der Regel einfacher Vorgang. Wenn das System oder die Anwendung jedoch fehlschlägt, während eine Anwendung Informationen auf einem Datenträger aktualisiert, kann das Ergebnis schwerwiegende Folgen haben, da die Benutzerdaten durch einen Dateiaktualisierungsvorgang beschädigt werden können, der teilweise abgeschlossen ist. Stabile Anwendungen führen häufig komplexe Sequenzen von Dateikopien und Dateibenennungen durch, um sicherzustellen, dass Daten nicht beschädigt werden, wenn ein System ausfällt.

Mit TxF ist es für eine Anwendung einfach, Dateiupdatevorgänge vor System- oder Anwendungsfehlern zu schützen. Um eine Datei sicher zu aktualisieren, öffnet die Anwendung die Datei im Transaktionsmodus, führt die erforderlichen Updates durch und führt dann einen Commit für die Transaktion aus. Wenn das System oder die Anwendung während des Dateiupdates fehlschlägt, stellt TxF die Datei automatisch in den Zustand wieder her, den sie vor Dem Beginn des Dateiupdates hatte, wodurch Dateibeschädigungen vermieden werden.

## <a name="multi-file-updates"></a>Updates für mehrere Dateien

TxF ist noch wichtiger, wenn ein einzelner logischer Vorgang mehrere Dateien betrifft. Wenn Sie beispielsweise ein Tool verwenden möchten, um eine der HTML- oder ASP-Seiten auf einer Website umzubenennen, würde ein gut entworfenes Tool auch alle Links korrigieren, um den neuen Dateinamen zu verwenden. Bei einem Fehler während dieses Vorgangs befindet sich die Website jedoch in einem inkonsistenten Zustand, wobei einige der Links weiterhin auf den alten Dateinamen verweisen. Indem der Dateibenennungsvorgang und der Linkfixierungsvorgang zu einer einzelnen Transaktion werden, stellt TxF sicher, dass die Datei umbenennen und die Verknüpfungskorrektur als einzelner Vorgang erfolgreich oder fehlgeschlagen ist.

## <a name="consistent-concurrent-updates"></a>Konsistente gleichzeitige Updates

TxF isoliert gleichzeitige Transaktionen. Wenn eine Anwendung eine Datei für einen Transaktionslesevorgang öffnet, während eine andere Anwendung dieselbe Datei für ein Transaktionsupdate geöffnet hat, isoliert TxF die Auswirkungen der beiden Transaktionen voneinander. Anders ausgedrückt: Der Transaktionsleser sieht immer eine einzelne, konsistente Version der Datei, auch wenn diese Datei gerade von einer anderen Transaktion aktualisiert wird.

Eine Anwendung kann diese Funktion verwenden, um Kunden das Anzeigen von Dateien zu ermöglichen, während andere Kunden Updates vornehmen. Beispielsweise kann ein Transaktionswebserver eine einzelne, konsistente Ansicht der Dateien bereitstellen, während ein anderes Tool diese Dateien gleichzeitig aktualisiert.

> [!Note]  
> TxF unterstützt keine gleichzeitigen Updates von mehreren Writern in verschiedenen Transaktionen. TxF unterstützt nur einen einzelnen Writer mit mehreren gleichzeitigen und konsistenten Readern.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Koordinieren mit anderen transaktiven Ressourcen-Managern

Transaktionen, die mit transaktiven Dateisystemen verwendet werden, können auch mit der transaktionierten Registrierung verwendet werden. Aktualisierungen der Datei und der Registrierung werden mit einer einzelnen Transaktion koordiniert.

Mithilfe [von Distributed Transaction Coordinator-Transaktionen](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) oder System.Transactions können Updates, die an SQL, MSMQ und anderen Transaktionsressourcen vorgenommen werden, mit Transaktionsdateiupdates koordiniert werden. Weitere Informationen finden Sie unter [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))von DTC.

## <a name="unsupported-scenarios"></a>Nicht unterstützte Szenarien

TxF unterstützt die folgenden Transaktionsszenarien nicht:

-   Transaktionen auf Netzwerkvolumes, z. B. auf Dateifreigaben. TxF wird von den CIFS-/SMB-Protokollen nicht unterstützt.
-   Transaktionen in einem anderen Dateisystem als NTFS.
-   Transaktionsvorgänge für Dateien, die vom clientseitigen Zwischenspeichern zwischengespeichert werden.
-   Dateizugriff mithilfe von Objekt-IDs.
-   Alle Szenarien mit freigegebenen Writern.
-   Jede Situation, in der eine Datei für einen längeren Zeitraum (Tage oder Wochen) geöffnet wird.

 

 
