---
description: Dieser Abschnitt bietet eine Übersicht über die Aufteilung der Verantwortung zwischen den Ws2-32.dll \_ und Transportdienstanbietern.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: Transportverteilung der Zuständigkeiten zwischen DLL und Dienstanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c256cb03bcc9e3f8746db5196c21fc2de0a8b157304a205587b275acc0bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733220"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>Transportverteilung der Zuständigkeiten zwischen DLL und Dienstanbietern

Dieser Abschnitt bietet eine Übersicht über die Aufteilung der Verantwortung zwischen den Ws2-32.dll \_ und Transportdienstanbietern.

## <a name="ws2_32dll-functionality-for-transport"></a>\_Ws232.dll Funktionen für den Transport

Die Hauptaufgabe des Datentransportanteils der Ws2-32.dll besteht darin, als Traffic Manager zwischen \_ Dienstanbietern und Anwendungen zu dienen. Da mehrere verschiedene Dienstanbieter mit derselben Anwendung interagieren, interagiert jeder Dienstanbieter streng mit dem \_ Ws2-32.dll. Die DLL kümmert sich um:

-   Auswählen eines geeigneten Dienstanbieters zum Erstellen von Sockets basierend auf einer Protokollbeschreibung.
-   Weiterleiten von Anwendungsprozeduraufrufen mit einem Socket an den entsprechenden Dienstanbieter, der diesen Socket erstellt hat oder steuert. Dienstanbieter sind sich nicht bewusst, dass dies geschieht.

Sie müssen sich keine Sorgen um die Details der Bzw. sogar um das Vorhandensein anderer Dienstanbieter machen. Durch abstrahieren der Dienstanbieter in einer konsistenten DLL-Schnittstelle und Ausführen dieser automatischen Routingfunktion für Datenverkehr ermöglicht die Ws2-32.dll Anwendungen die Interaktion mit einer Vielzahl von Anbietern, ohne dass die Anwendungen die Aufteilungen zwischen Anbietern kennen müssen, in denen verschiedene Anbieter installiert \_ sind.

Die Ws232.dll basiert auf den Parametern der \_ API-Socketerstellungsfunktionen ( [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)), um zu bestimmen, welcher Dienstanbieter verwendet werden soll. Der ausgewählte Transportdienstanbieter wird über die [**WSPSocket-Funktion**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) aufgerufen. Im Fall der  Socketfunktion findet die Ws2-32.dll den ersten Eintrag in der Gruppe installierter \_  [**WSAPROTOCOL \_ INFO-Strukturen,**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) die mit den Werten in dem Tupel aus den Parametern ( Adressfamilie, Sockettyp, Protokoll ) kompatibel sind. Um die Abwärtskompatibilität zu gewährleisten, behandelt die Ws2-32.dll den Wert 0 (null) für die Adressfamilie oder den Sockettyp als \_ Platzhalterwert.   Der Wert 0 (null) für das Protokoll wird vom Ws2-32.dll nicht als Platzhalterwert betrachtet, es sei denn, ein solches Verhalten wird für ein bestimmtes Protokoll angegeben, indem das FLAG PFL MATCHES PROTOCOL ZERO in der \_ \_ \_ \_ **WSAPROTOCOL \_ INFO-Struktur** festgelegt ist.

Wenn für [**die WSASocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) NULL für *lpProtocolInfo* angegeben wird, ist das Verhalten genau wie für den Socket [**beschrieben.**](/windows/desktop/api/Winsock2/nf-winsock2-socket) Wenn jedoch auf eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) verwiesen wird, führt die Ws2-32.dll keine übereinstimmende Funktion aus, sondern leitet die Socketerstellungsanforderung sofort an den Transportdienstanbieter weiter, der der angegebenen \_ **WSAPROTOCOL \_ INFO-Struktur** zugeordnet ist. Die Werte für das Tupel (*Adressfamilie,* *Sockettyp,*) werden dem Dienstanbieter in der [**WSPSocket-Funktion**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) intakt bereitgestellt. Dienstanbieter können die Werte der Parameter (*Adressfamilie,*  Sockettyp, ) entsprechend ignorieren oder beachten. Sie dürfen jedoch  keinen Fehlerzustand angeben, wenn der Wert der Adressfamilie oder des Sockettyps 0 (null) ist.  Darüber hinaus dürfen Dienstanbieter keine Fehlerbedingung angeben, wenn die Manifestkonst constant FROM PROTOCOL INFO in einem der \_ Parameter ( Adressfamilie, Sockettyp, ) enthalten \_ ist.  Dieser Wert gibt einfach an, dass die Anwendung die Werte in den entsprechenden Parametern der **WSAPROTOCOL \_ INFO-Struktur** verwenden möchte: (**iAddressFamily**, **iSocketType**, **iProtocol**).

Im Rahmen der Socketerstellung informiert ein Dienstanbieter die Ws2-32.dll über die Zuordnung zwischen sich selbst und dem neuen Socket mit parametern, die an \_ [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) oder [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle)übergeben werden. Der Ws232.dll verfolgt diese Zuordnung \_ zwischen Sockethandles und bestimmten Dienstanbietern nach. Wenn eine Anwendungsschnittstellenfunktion aufgerufen wird, die auf ein Sockethand handle verweist, sucht die Ws2-32.dll die Zuordnung und ruft die entsprechende Dienstanbieterschnittstellenfunktion des entsprechenden Dienstanbieters \_ auf.

Zusätzlich zum Hauptdienst für das Datenverkehrsrouting stellt die Ws2-32.dll eine Reihe anderer Dienste wie die Protokollenumeration zur Verfügung. Socketdeskriptorverwaltung (Zuordnung, Freigabe und Kontextwertzuordnung) für Nichtdateisystem-Dienstanbieter, Blockieren der Hookverwaltung pro Thread, Bytetausch-Hilfsprogramme, Warteschlangen von asynchronen Prozeduraufrufen (APCs), um den Aufruf von E/A-Abschlussroutinen zu ermöglichen, und Versionsaushandlung zwischen Anwendungen und \_ dem Ws2-32.dll sowie zwischen \_ Ws2-32.dll und Dienstanbietern. \_

## <a name="transport-service-provider-functionality"></a>Funktionen des Transportdienstanbieters

Dienstanbieter implementieren das eigentliche Transportprotokoll, das Funktionen wie das Einrichten von Verbindungen, das Übertragen von Daten, das Ausführen der Flusssteuerung und Fehlersteuerung usw. umfasst. Der Ws232.dll weiß nicht, wie Anforderungen an Dienstanbieter realisiert werden. Dies liegt an der Implementierung \_ des Dienstanbieters. Die Implementierung solcher Funktionen kann sich von Anbieter zu Anbieter stark unterscheiden. Dienstanbieter blenden die implementierungsspezifischen Details zur Durchführung von Netzwerkvorgängen aus.

Transportdienstanbieter können grob in zwei Kategorien unterteilt werden: solche, deren Socketdeskriptoren echte Dateisystemhandles sind (und nachfolgend als INSTALLABLE FILE SYSTEM-Anbieter (IFS) bezeichnet werden. Der Rest wird als Nicht-IFS-Anbieter bezeichnet. Der Ws2-32.dll übergibt den Socketdeskriptor des Transportdienstanbieters immer an die Windows Sockets-Anwendung, sodass Anwendungen die Socketdeskriptoren nutzen können, die dateisystemhandles sind, wenn sie \_ dies möchten.

Zusammengefasst: Dienstanbieter implementieren die netzwerkspezifischen Protokolle auf niedriger Ebene. Der Ws232.dll stellt die mittlere Datenverkehrsverwaltung zur Verfügung, die diese \_ Transportprotokolle mit Anwendungen verbindet. Anwendungen stellen wiederum die Richtlinie zur Verfügung, wie diese Datenverkehrsströme und netzwerkspezifischen Vorgänge verwendet werden, um die vom Benutzer gewünschten Funktionen zu erfüllen.

 

 
