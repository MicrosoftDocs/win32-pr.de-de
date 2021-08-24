---
title: BITS-Schnittstellen
description: Verwenden Sie die folgenden Background Intelligent Transfer Service -Schnittstellen (BITS), um Dateien zu übertragen und Aufträge in der Übertragungswarteschlange zu überwachen.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: 0edd4229e76a85767689427cfccd6cb38aa11c0e54345053ce10d1a99fc1fde8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529070"
---
# <a name="bits-interfaces"></a>BITS-Schnittstellen

Verwenden Sie die folgenden Background Intelligent Transfer Service -Schnittstellen (BITS), um [Dateien zu übertragen und Aufträge in](using-bits.md) der Übertragungswarteschlange zu überwachen.

| Schnittstelle | BESCHREIBUNG |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | Clients implementieren die [**IBackgroundCopyCallback-Schnittstelle,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen, geändert oder ein Fehler aufgetreten ist. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | Clients implementieren die [**IBackgroundCopyCallback2-Schnittstelle,**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) um eine Benachrichtigung zu erhalten, dass das Herunterladen einer Datei abgeschlossen wurde. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | Clients implementieren die [**IBackgroundCopyCallback3-Schnittstelle,**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) um Benachrichtigungen zu erhalten, dass der Download von Bereichen einer Datei abgeschlossen wurde. |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Ruft Details zu einem Auftragsfehler ab. |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Ruft die lokalen und Remotedateinamen einer Dateiübertragungsanforderung im Auftrag und dessen Status ab. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Gibt einen neuen Remotenamen für die Datei an und ruft die Liste der herunterzuladenden Bereiche ab. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Überprüft die Datei, damit Peers ihren Inhalt anfordern können, und ruft den Namen der temporären Datei ab. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Ruft Downloadstatistiken für Peers und Ursprungsserver ab. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Stellt generische Get- und Set-Methoden für BackgroundCopyFile-Eigenschaften zur Verfügung. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Ruft generische Eigenschaften von BITS-Dateiübertragungen ab oder legt sie fest. |
| [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Fügt dem Auftrag Dateien hinzu, legt die Prioritätsebene des Auftrags fest, bestimmt den Status des Auftrags und startet und beendet den Auftrag. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Ruft Antwortdaten aus einem Uploadauftrag ab, bestimmt den Fortschritt der Antwortdatenübertragung an den Client, fordert die Befehlszeilenausführung an und stellt Anmeldeinformationen für einen Proxy und einen Remoteserver zur Verfügung. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Lädt Bereiche einer Datei herunter, ändert das Präfix eines Remotedateinamens und verwaltet die Besitzer- und ACL-Informationen mit der Datei. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Ermöglicht die Peerzwischenspeicherung, schränkt die Downloadzeit ein und überprüft die Merkmale von Benutzertoken. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Fragt mehrere optionale Verhaltensweisen eines Auftrags ab oder legt sie fest. |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Gibt Clientzertifikate für die zertifikatbasierte Clientauthentifizierung und benutzerdefinierte Header für HTTP-Anforderungen an. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Verwenden Sie diese Schnittstelle, um die für eine BITS-Übertragung verwendete HTTP-Methode abzurufen und/oder zu überschreiben. |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Erstellt Übertragungsaufträge, ruft ein Enumeratorobjekt von Aufträgen in der Warteschlange ab und ruft einzelne Aufträge aus der Warteschlange ab. |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Ruft Informationen zu einem Peer in der Umgebung ab. |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Verwalten Sie den Pool von Peers, aus dem Sie Inhalte herunterladen können. |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Ruft Informationen zu einer Datei im Cache ab. |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Ordnet ein Sicherheitstokenpaar für einen BITS-Übertragungsauftrag (Background Intelligent Transfer Service) zu und verwaltet es. |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Aufzählen von Dateien im Auftrag. |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Aufzählen von Aufträgen in der Übertragungswarteschlange. |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Enumeriert die Datensätze des Caches. |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Listet die Peers auf, die BITS gefunden hat. |



 

 

 




