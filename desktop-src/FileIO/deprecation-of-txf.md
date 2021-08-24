---
description: In diesem Thema werden Alternativen zur Verwendung der TRANSAKTIONAL NTFS-API (TxF) in gängigen Verwendungsszenarien erläutert.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternativen zur Verwendung von Transaktions-NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab924c5ee4204180b891b3aad13a5809fa07671ad0e18d6ddc9ce353122ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765970"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternativen zur Verwendung von Transaktions-NTFS

-   [Zusammenfassung](#abstract)
-   [Introduction (Einführung)](#introduction)
-   [Alternativen zu TxF nach Szenario](#alternatives-to-txf-by-scenario)
-   [Anwendungen, die eine einzelne Datei mit dokumentspezifischen Daten aktualisieren](#applications-updating-a-single-file-with-document-like-data)
-   [Anwendungen, die Updates für mehrere Dateien und/oder die Registrierungsstruktur ausführen](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Anwendungen, die einen Satz strukturierter Daten verwalten](#applications-managing-a-set-of-structured-data)
-   [Anwendungen mit Transaktionen, die Dateien auf einem lokalen NTFS-Volume und Tabellen in einer externen SQL enthalten](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Schließen & empfohlenen Aktion](/windows)

## <a name="abstract"></a>Zusammenfassung

Microsoft empfiehlt Entwicklern dringend, die erläuterten Alternativen zu verwenden (oder in einigen Fällen andere Alternativen zu untersuchen), anstatt eine API-Plattform zu verwenden, die in zukünftigen Versionen von Windows.

## <a name="introduction"></a>Einführung

TxF wurde mit Windows Vista eingeführt, um atomarer Dateitransaktionen in die Windows. Sie ermöglicht es Windows-Entwicklern, transaktionale Atomarität für Dateivorgänge in Transaktionen mit einer einzelnen Datei, in Transaktionen, die mehrere Dateien enthalten, und in Transaktionen, die mehrere Quellen wie z. B. die Registrierung (über TxR) und Datenbanken (z. B. SQL) umfasst, zu verwenden. TxF ist zwar ein leistungsstarker Satz von APIs, aber seit Windows Vista gab es aufgrund seiner Komplexität und verschiedener Nuancen, die Entwickler im Rahmen der Anwendungsentwicklung berücksichtigen müssen, äußerst eingeschränktes Interesse an dieser API-Plattform. Daher erwägt Microsoft, TxF-APIs in einer zukünftigen Version von Windows als veraltet zu betrachten, um die Entwicklungs- und Wartungsbemühungen auf andere Features und APIs zu konzentrieren, die für eine größere Mehrheit der Kunden einen höheren Nutzen haben. Im nächsten Abschnitt werden alternative Beispielmethoden beschrieben, um ähnliche Ergebnisse wie TxF für verschiedene Anwendungsszenarien zu erzielen.

## <a name="alternatives-to-txf-by-scenario"></a>Alternativen zu TxF nach Szenario

Mit den oben beschriebenen Einschränkungen sollten Entwickler Alternativen zu TxF untersuchen, um Anwendungsszenarien abdecken zu können, die von TxF nicht erfüllt werden. Hier werden einige empfohlene Alternativen zu gängigen TxF-Verwendungsmöglichkeiten für Entwickler erläutert. Beachten Sie, dass diese Liste weder vollständig noch vollständig ist.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Anwendungen, die eine einzelne Datei mit dokumentspezifischen Daten aktualisieren

Viele Anwendungen, die sich mit "dokumentspezifischen" Daten befassen, neigen dazu, das gesamte Dokument in den Arbeitsspeicher zu laden, darauf zu arbeiten und es dann zurück zu schreiben, um die Änderungen zu speichern. Die benötigte Uneinheitlichkeit besteht hier in der vollständigen oder gar nicht angewendeten Änderung, da ein inkonsistenter Zustand die Datei beschädigt machen würde. Ein gängiger Ansatz ist, das Dokument in eine neue Datei zu schreiben und dann die ursprüngliche Datei durch die neue datei zu ersetzen. Eine Methode hierzu ist die [**ReplaceFile-API.**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Anwendungen, die Updates für mehrere Dateien und/oder die Registrierungsstruktur ausführen

Es gibt viele Anwendungen, die atomisch ein Update für einen Satz von Dateien und für die Registrierung ausführen müssen. Dieses Szenario wird am häufigsten durch eine Installationsprogrammanwendung erreicht, z. B. Windows Installer. Weitere Informationen zum Windows-Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Anwendungen, die einen Satz strukturierter Daten verwalten

Viele Anwendungen verwalten einige proprietäre Datenstrukturen unterschiedlicher Typen als Mittel zum Speichern von Daten. Eine erhebliche Herausforderung für diese Anwendungen besteht darin, die Integrität interner Zeiger/Verweise zu gewährleisten, wenn während eines Aktualisierungsvorgangs ein Fehler auftritt. Die Erstellung des Mechanismus dafür ist tatsächlich ein "schwieriges Problem", und daher verlassen sich die meisten Anwendungen auf einen echten Datenbankserver, um ihr Dataset zu verwalten.

Es gibt zwei Vorschläge für die Verwaltung strukturierter Daten:

-   Microsoft stellt den Ese-Posteingang (Extensible Storage Engine) in Windows bereit, um Anwendungen das Ausführen von Transaktionsaktualisierungs- und -abrufvorgängen zu ermöglichen. Weitere Informationen zur Extensible Storage Engine (ESE) finden Sie unter <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Für Anwendungen, die einen leistungsfähigeren, robusteren und skalierbareren Datenbankanbieter benötigen, wird empfohlen, dass Kunden die Verwendung des filestream-Features in Erwägung ziehen, das für Microsoft SQL Server. Weitere Informationen zu SQL Filestreams finden Sie unter <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Anwendungen mit Transaktionen, die Dateien auf einem lokalen NTFS-Volume und Tabellen in einer externen SQL enthalten

Es gibt Klassen von Anwendungen, die entweder große Datasetanforderungen haben oder transaktionale Atomarität in einem Vorgang mit einer externen Datenbank und lokalem Speicher benötigen. In diesem Szenario wird dringend empfohlen, dass Entwickler erwägen, SQL Filestreams zum Ausführen von Transaktionsdateivorgängen zu verwenden. Weitere Informationen zu SQL Filestreams finden Sie unter <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Schließen & empfohlenen Aktion

TxF ist ein komplexer und differenzierter Satz von APIs, die häufig nicht von Anwendungen von Drittanbietern verwendet werden. Mit der Möglichkeit, dass diese APIs in zukünftigen Versionen von Windows möglicherweise nicht verfügbar sind, und der Tatsache, dass es einfachere alternative Mittel gibt, um viele der Szenarien zu erreichen, für die TxF entwickelt wurde, empfiehlt Microsoft Entwicklern dringend, diese alternativen Mittel zu untersuchen, anstatt eine Abhängigkeit von TxF in ihren Anwendungen zu erstellen.

 

 
