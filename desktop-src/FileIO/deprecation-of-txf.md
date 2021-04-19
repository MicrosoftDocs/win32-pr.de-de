---
description: In diesem Thema werden Alternativen zur Verwendung der Transaktions-NTFS-API (TxF) in gängigen Verwendungs Szenarios erläutert.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternativen zur Verwendung von transaktionalen NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc69974f27abfba0323ea4d3f16a720e5e99e69d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372965"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternativen zur Verwendung von transaktionalen NTFS

-   [Kter](#abstract)
-   [Introduction (Einführung)](#introduction)
-   [Alternativen zu TxF nach Szenario](#alternatives-to-txf-by-scenario)
-   [Anwendungen, die eine einzelne Datei mit "Dokument ähnlichen" Daten aktualisieren](#applications-updating-a-single-file-with-document-like-data)
-   [Anwendungen, die Updates für mehrere Dateien und/oder für die Registrierungs Struktur durchführen](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Anwendungen, die einen Satz strukturierter Daten verwalten](#applications-managing-a-set-of-structured-data)
-   [Anwendungen mit Transaktionen, die Dateien auf einem lokalen NTFS-Volume und Tabellen in einer externen SQL-Datenbank betreffen](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Schließen & empfohlenen Aktion](/windows)

## <a name="abstract"></a>Zusammenfassung

Microsoft empfiehlt Entwicklern dringend, die behandelten Alternativen zu untersuchen (oder in einigen Fällen andere Alternativen zu untersuchen), anstatt eine API-Plattform zu verwenden, die in zukünftigen Versionen von Windows möglicherweise nicht verfügbar ist.

## <a name="introduction"></a>Einführung

TxF wurde mit Windows Vista eingeführt, um atomarische Dateitransaktionen in Windows einzuführen. Dadurch können Windows-Entwickler eine transaktionale Atomizität für Datei Vorgänge in Transaktionen mit einer einzelnen Datei, in Transaktionen, die mehrere Dateien betreffen, und in Transaktionen, die mehrere Quellen umfassen – wie z. b. die Registrierung (durch TxR) und Datenbanken (z. b. SQL), haben. Obwohl es sich bei TxF um einen leistungsfähigen Satz von APIs handelt, ist für diese API-Plattform sehr wenig Entwickler Interesse, da Windows Vista hauptsächlich aufgrund der Komplexität und der verschiedenen Nuancen, die Entwickler im Rahmen der Anwendungsentwicklung berücksichtigen müssen, wichtig ist. Daher ist Microsoft in Erwägung gezogen, TxF-APIs in einer zukünftigen Windows-Version als veraltet zu kennzeichnen, um Entwicklungs-und Wartungsmaßnahmen auf andere Features und APIs zu konzentrieren, die für eine größere Mehrheit von Kunden mehr nutzen. Der nächste Abschnitt beschreibt alternative Beispiel Methoden, um ähnliche Ergebnisse zu erzielen, wie TxF für verschiedene Typen von Anwendungsszenarien verwendet.

## <a name="alternatives-to-txf-by-scenario"></a>Alternativen zu TxF nach Szenario

Mit den oben beschriebenen Einschränkungen sollten Entwickler Alternativen zu TxF untersuchen, um Anwendungs Szenarios abzudecken, die von TxF nicht erfüllt werden. Hier finden Sie einige Vorschläge für allgemeine Verwendungsmöglichkeiten von TxF für Entwickler. Beachten Sie, dass diese Liste weder vollständig noch vollständig ist.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Anwendungen, die eine einzelne Datei mit "Dokument ähnlichen" Daten aktualisieren

Viele Anwendungen, die "Dokument ähnliche" Daten verarbeiten, laden tendenziell das gesamte Dokument in den Arbeitsspeicher, arbeiten darauf und schreiben es zurück, um die Änderungen zu speichern. Die erforderliche Atomizität besteht darin, dass die Änderungen entweder vollständig angewendet oder überhaupt nicht angewendet werden, da die Datei durch einen inkonsistenten Zustand beschädigt wird. Ein gängiger Ansatz besteht darin, das Dokument in eine neue Datei zu schreiben und dann die ursprüngliche Datei durch die neue Datei zu ersetzen. Eine Methode hierfür ist die [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) -API.

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Anwendungen, die Updates für mehrere Dateien und/oder für die Registrierungs Struktur durchführen

Es gibt viele Anwendungen, die atomarisch ein Update für eine Gruppe von Dateien und für die Registrierung ausführen müssen. Dieses Szenario wird in der Regel durch eine installeranwendung, wie z. b. Windows Installer, erreicht. Weitere Informationen zu Windows Installer finden Sie unter [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Anwendungen, die einen Satz strukturierter Daten verwalten

Viele Anwendungen verwalten einige proprietäre Datenstrukturen unterschiedlicher Typen als Mittel zum Speichern von Daten. Eine bedeutende Herausforderung für diese Anwendungen ist der Prozess der Aufrechterhaltung der Integrität Interner Zeiger/Verweise, wenn während eines Aktualisierungs Vorgangs ein Fehler auftritt. Das Erstellen des Mechanismus hierfür ist tatsächlich ein "Schwerpunkt", und daher verlassen sich die meisten Anwendungen auf einen echten Datenbankserver, um das DataSet zu verwalten.

Zwei Vorschläge für die Verwaltung strukturierter Daten sind:

-   Microsoft stellt die ESE-Eingangsbox (Extensible Storage Engine) in Windows bereit, damit Anwendungen transaktive Daten Aktualisierungs-und Abruf Vorgänge ausführen können. Weitere Informationen zur Extensible Storage Engine (ESE) finden Sie unter <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Für Anwendungen, die einen leistungsfähigeren, robusten und skalierbaren Datenbankanbieter benötigen, empfiehlt es sich, die FILESTREAM-Funktion zu verwenden, die mit Microsoft SQL Server verfügbar ist. Weitere Informationen zu SQL-filestreams finden Sie unter <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Anwendungen mit Transaktionen, die Dateien auf einem lokalen NTFS-Volume und Tabellen in einer externen SQL-Datenbank betreffen

Es gibt Anwendungs Klassen, die entweder über große datasetanforderungen verfügen oder transaktionale Atomizität in einem Vorgang mit externer Datenbank und lokalem Speicher aufweisen müssen. In diesem Szenario wird dringend empfohlen, dass Entwickler SQL-filestreams verwenden, um Transaktions Datei Vorgänge auszuführen. Weitere Informationen zu SQL-filestreams finden Sie unter <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Schließen & empfohlenen Aktion

TxF ist ein komplexer und differenzierter Satz von APIs, die nicht häufig von Anwendungen von Drittanbietern verwendet werden. Mit der Möglichkeit, dass diese APIs in zukünftigen Versionen von Windows möglicherweise nicht verfügbar sind, und die Tatsache, dass es eine einfachere Alternative bedeutet, viele der Szenarien zu erreichen, für die TxF entwickelt wurde, empfiehlt Microsoft Entwicklern dringend, diese alternativen Mittel zu untersuchen, anstatt eine Abhängigkeit von TxF in Ihren Anwendungen zu erstellen.

 

 
