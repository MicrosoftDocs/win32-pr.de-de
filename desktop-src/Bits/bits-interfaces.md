---
title: Bits-Schnittstellen
description: Verwenden Sie die folgenden Background Intelligent Transfer Service Bits-Schnittstellen, um Dateien zu übertragen und Aufträge innerhalb der Übertragungs Warteschlange zu überwachen.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: fc95d4aea6d6d74ff2952cf2ef686fbaa1049732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947422"
---
# <a name="bits-interfaces"></a>Bits-Schnittstellen

Verwenden Sie die folgenden Background Intelligent Transfer Service Bits-Schnittstellen, um [Dateien zu übertragen und Aufträge](using-bits.md) innerhalb der Übertragungs Warteschlange zu überwachen.

| Schnittstelle | BESCHREIBUNG |
|-|-|
| [**Ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | Clients implementieren die [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen, geändert oder fehlerhaft ist. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | Clients implementieren die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle, um Benachrichtigungen zu erhalten, dass eine Datei den Download abgeschlossen hat. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | Clients implementieren die [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) -Schnittstelle, um eine Benachrichtigung zu erhalten, dass die Bereiche einer Datei den Download abgeschlossen haben. |
| [**Ibackgroundcopyerror**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Ruft die Details eines Auftrags Fehlers ab. |
| [**Ibackgroundcopyfile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Ruft die lokalen und Remote Dateinamen einer Datei Übertragungs Anforderung im Auftrag und ihren Fortschritt ab. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Gibt einen neuen Remote Namen für die Datei an und ruft die Liste der herunter zuladenden Bereiche ab. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Überprüft die Datei, damit Peers ihren Inhalt anfordern und den Namen der temporären Datei abrufen können. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Ruft Download Statistiken für Peers und Ursprungsserver ab. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Stellt generische Eigenschaften get-und Set-Methoden für backgroundcopyfile-Eigenschaften bereit. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Ruft generische Eigenschaften von BITS-Dateiübertragungen ab oder legt Sie fest. |
| [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Fügt dem Auftrag Dateien hinzu, legt die Prioritätsstufe des Auftrags fest, bestimmt den Status des Auftrags und startet und beendet den Auftrag. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Ruft Antwortdaten von einem Uploadauftrag ab, bestimmt den Fortschritt der Antwortdaten Übertragung an den Client, fordert die Befehlszeilen Ausführung an und stellt Anmelde Informationen für einen Proxy und einen Remote Server bereit. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Lädt die Bereiche einer Datei herunter, ändert das Präfix eines Remote Dateinamens und verwaltet den Besitzer und die ACL-Informationen mit der Datei. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Aktiviert die Peer Zwischenspeicherung, schränkt die Downloadzeit ein und überprüfen die Merkmale von Benutzer Token. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Fragt mehrere optionale Verhalten eines Auftrags ab oder legt diese fest. |
| [**Ibackgroundcopyjobhttpoptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Gibt Client Zertifikate für die Zertifikat basierte Client Authentifizierung und benutzerdefinierte Header für HTTP-Anforderungen an. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Verwenden Sie diese Schnittstelle, um die für eine Bits-Übertragung verwendete HTTP-Methode abzurufen und/oder zu überschreiben. |
| [**Ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Erstellt Übertragungs Aufträge, Ruft ein Enumeratorobjekt von Aufträgen in der Warteschlange ab und ruft einzelne Aufträge aus der Warteschlange ab. |
| [**Ibitspeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Ruft Informationen zu einem Peer in der Umgebung ab. |
| [**Ibitspeercacheadministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Verwalten Sie den Pool von Peers, von dem Sie Inhalte herunterladen können. |
| [**Ibitspeercacherecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Ruft Informationen zu einer Datei im Cache ab. |
| [**Ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Verknüpft und verwaltet ein paar von Sicherheits Token für einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits). |
| [**Ienumbackgroundcopyfiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Listet die Dateien im Auftrag auf. |
| [**Ienumbackgroundcopyjobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Listet Aufträge in der Übertragungs Warteschlange auf. |
| [**Ienumbitspeercacherecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Listet die Datensätze des Caches auf. |
| [**Ienumbitspeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Listet die von Bits ermittelten Peers auf. |



 

 

 




