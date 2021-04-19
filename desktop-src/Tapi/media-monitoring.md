---
description: Wenn sich ein-Rückruf im verbundenen Zustand befindet, können Daten über den-Befehl transportiert werden. Der Typ des aufrufmediums gibt Aufschluss über den Datentyp (z. b. den Datentyp oder das Protokoll der höheren Ebene) dieses Medien Stroms.
ms.assetid: 3281387e-3f72-4fda-8199-b3ce6e45e910
title: Medienüberwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb54989306fd80c48c0b99c9f8285a83b40bed25
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364289"
---
# <a name="media-monitoring"></a>Medienüberwachung

Wenn sich ein-Rückruf im *verbundenen* Zustand befindet, können Daten über den-Befehl transportiert werden. Der Typ des aufrufmediums gibt Aufschluss über den Datentyp (z. b. den Datentyp oder das Protokoll der höheren Ebene) dieses Medien Stroms.

TAPI ermöglicht die Bereitstellung von Anwendungen mit einer Benachrichtigung über Änderungen im Medientyp eines Aufrufes. Die Benachrichtigung enthält einen Hinweis auf den neuen Medientyp des Aufrufes. Der Dienstanbieter entscheidet, wie er diese Bestimmung treffen will. Der Dienstanbieter könnte z. b. die Signalverarbeitung des Mediendaten Stroms verwenden, um den Medientyp zu bestimmen, oder er kann auf unterschiedlichen Klingeln Mustern, die anderen Medienströmen zugewiesen sind, oder auf Informations Elementen basieren, die in einem Out-of-Band-Signalisierungs Protokoll weitergegeben werden. Unabhängig davon, wie die Medientyp Bestimmung erreicht wird, wird die Anwendung einfach über Änderungen des Medientyps eines vorhandenen Aufrufes informiert.

Weitere Informationen und eine Liste der derzeit definierten TAPI-Medientypen oder-Modi finden Sie unter [linemediamode- \_ Konstanten](linemediamode--constants.md). Dienstanbieter können anbieterspezifische Medientypen für hoch spezialisierte Geräte implementieren. Informationen zu diesen finden Sie in der Gerätedokumentation.

Die von TAPI definierten Medientypen umfassen Folgendes:

-   Unbekannt Der Medientyp des Aufrufes ist zurzeit nicht bekannt – der-Befehl ist nicht klassifiziert.
-   Interaktive Stimme. Beim Anruf wurde Voice Energy erkannt, und der Anruf wird als interaktiver Sprachanruf mit einer Person am Ende der Anwendung behandelt.
-   Automatisierte Stimme. Beim Anruf wurde Voice Energy erkannt, und der Anruf wird als Sprachanruf behandelt, aber ohne eine Person am Ende der Anwendung, z. b. mit einer beantworteten Computeranwendung.
-   Datenmodem. Eine Modem Sitzung für den-Befehl. Aktuelle Modem Protokolle erfordern, dass die aufgerufene Station den Handshake initiiert. Für einen eingehenden Datenmodem Anrufe kann die Anwendung normalerweise keine positive Erkennung durchführen. Wie der Dienstanbieter diese Bestimmung trifft, ist seine Wahl. So kann z. b. ein Ruhe Zeitraum nur nach dem Beantworten eines eingehenden Aufrufes als Heuristik verwendet werden, um zu entscheiden, dass dies ein Datenmodem Anruf sein könnte.
-   G3-Fax. Eine faxsitzung der Gruppe 3 für den-Befehl.
-   G4-Fax. Eine Fax-Sitzung der Gruppe 4 für den-Befehl.
-   TDD. Der Medienstrom des Aufrufes verwendet die Telefoniegeräte für das Gehörlose Protokoll.
-   Digitale Daten. Ein digitaler Datenstrom des nicht angegebenen Formats.
-   Teletex, Videotex, Telex, gemischt. Diese entsprechen den telematischen Diensten mit denselben Namen.
-   ADSI. Eine analoge Anzeige Dienste-Schnittstellen Sitzung für den-Befehl. ADSI erweitert Sprachanrufe mit alphanumerischen Informationen, die auf das Telefon heruntergeladen wurden, und verwendet weiche Schaltflächen auf dem Telefon.

Eine Anwendung kann die Medienüberwachung für einen angegebenen-Befehl mit [**linemonitormedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia)aktivieren bzw. deaktivieren. Die Anwendung gibt an, welche Medientypen Sie überwachen möchten. wenn die Medienüberwachung aktiviert ist, wird die Anwendung durch die Erkennung einer Medientyp Änderung mit der [**Zeile \_ monitormedia**](line-monitormedia.md) -Nachricht benachrichtigt. Diese Meldung enthält das Telefon handle, für das die Medientyp Änderung erkannt wurde, sowie den neuen Medientyp.

Es gibt einen Unterschied zwischen dem Medientyp eines Aufrufes, der von [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) gemeldet wird, und den Media Type-Ereignis Berichten von Zeilen \_ monitormedia-Meldungen. Der Medientyp eines Aufrufes wird ausschließlich von Besitzer Anwendungen des Aufrufes bestimmt und nicht automatisch von Medien Überwachungs Ereignissen geändert. Die einzige Ausnahme ist die erste Medientyp Bestimmung, die von der TAPI-Dynamic-Link-Bibliothek durchgeführt werden kann, um den ersten Besitzer eines Aufrufes auszuwählen. In diesem Fall könnte man argumentieren, dass die Bibliothek der Besitzer des Aufrufes ist.

Die standardmäßige Medientyp Überwachung wird für die Medientypen ausgeführt, für die das Zeilen Gerät geöffnet wurde. Dadurch kann der Medientyp eines eingehenden Anrufes bestimmt werden, bevor der Aufruf an eine Anwendung basierend auf den Anforderungen der Anwendung übergeben wird. Der Bereich der Medienüberwachung eines Aufrufes wird durch die Lebensdauer des Aufrufes gebunden. Die Medienüberwachung bei einem-Rückruf wird beendet, sobald der-Rückruf die Verbindung *trennt oder in* den *Leerlauf* wechselt.

Eine Anwendung kann Geräte Bezeichner für verschiedene Geräteklassen abrufen, die einer geöffneten Zeile zugeordnet sind, indem [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)aufgerufen wird. Diese Funktion nimmt ein Zeilen handle, eine Adresse oder ein Rückruf Handle sowie eine Beschreibung der Geräteklasse an. Er gibt den Geräte Bezeichner für das Gerät der angegebenen Geräteklasse zurück, die dem Open-Line-Gerät, der Adresse oder dem-Befehl zugeordnet ist. Wenn die Geräteklasse "TAPI/Line" ist, wird der Geräte Bezeichner des Linien Geräts zurückgegeben. Wenn die Geräteklasse "MCI/Wave" ist, wird der Geräte Bezeichner eines MCI-waveaudiogeräts zurückgegeben (sofern unterstützt), wodurch Aktivitäten wie das Aufzeichnen oder Wiedergeben von Audiodaten über den-Befehl in der Zeile ermöglicht werden.

Die Anwendung kann die zurückgegebene Gerätekennung mit der entsprechenden Medien-API verwenden, um die Funktionen des Geräts abzufragen und anschließend das Medien Gerät zu öffnen. Wenn Ihre Anwendung z. b. die Zeile als Wellenform-Gerät verwenden muss, muss Sie zuerst [**waveingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) und/oder [**waveoutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) aufrufen, um die Wellenform-Funktionen des Geräts zu bestimmen. Das typische Wellenform-Datenformat, das von Telefonie in Nordamerika unterstützt wird, ist 8-Bit-m-Gesetz bei 8000-Stichproben pro Sekunde, obwohl der Wave-Gerätetreiber diese Stichprobenrate konvertieren und in andere allgemeinere Multimedia-Audioformate umwandeln kann.

Zum anschließenden Öffnen eines Zeilen Geräts für die Audiowiedergabe mithilfe der Wellenform-API ruft eine Anwendung [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)auf. Die Implementierung von **WaveOutOpen** ist gerätespezifisch, und es gibt eine Vielzahl von Optionen für die Implementierung dieser Funktion.

 

 
