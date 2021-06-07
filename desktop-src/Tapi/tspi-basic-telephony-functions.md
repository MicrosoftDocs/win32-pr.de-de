---
description: Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: GRUNDLEGENDE TSPI-Telefoniefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524154"
---
# <a name="tspi-basic-telephony-functions"></a>GRUNDLEGENDE TSPI-Telefoniefunktionen

Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren. Im Folgenden finden Sie eine Liste solcher Funktionen nach Kategorie. Eine Funktion wird als asynchron *identifiziert,* wenn sie die Vervollständigung in einer ANTWORT-Nachricht an die Anwendung angibt. Wenn die Funktion ihr Ergebnis immer sofort zurückgibt, wird die Funktion als synchron *betrachtet.*

-   [Adresses](#addresses)
-   [Beantworten eingehender Anrufe](#answering-incoming-calls)
-   [Drop-Funktionen für Aufrufe](#call-drop-functions)
-   [Aufrufzustände und Ereignisse](#call-states-and-events)
-   [Zeilenstatus und Funktionen](#line-status-and-capabilities)
-   [Zeilenversionsaushandlung](#line-version-negotiation)
-   [Tätigen von Aufrufen](#making-calls)
-   [Öffnen und Schließen von Line-Geräten](#opening-and-closing-line-devices)
-   [Telefonversionsaushandlung](#phone-version-negotiation)
-   [TSP-Initialisierung und -Herunterfahren](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>TSP-Initialisierung und -Herunterfahren



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**\_PROVIDERSPI-AnbieterInstallieren**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Installiert einen TSP. Synchronous.                              |
| [**\_TSPI-AnbieterInstallieren**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Installiert den TSP. Veraltet mit Version 2.0. Synchronous. |
| [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Initialisiert den TSP. Synchronous.                         |
| [**TSPI \_ providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Fährt den Dienstanbieter herunter.                          |
| [**PROVIDERSSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Entfernt einen TSP. Synchronous.                               |
| [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Entfernt einen TSP. Veraltet mit Version 2.0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Telefonversionsaushandlung



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Gibt die höchste SPI-Version zurück, unter der der Dienstanbieter für dieses Gerät arbeiten kann. |



 

## <a name="line-version-negotiation"></a>Zeilenversionsaushandlung



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Ermöglicht einer Anwendung das Aushandeln einer TSPI-Version für die Verwendung mit einem bestimmten Liniengerät. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Zeilenstatus und Funktionen



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Gibt die Funktionen eines bestimmten Liniengeräts zurück. Synchronous.                                                                                                  |
| [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Gibt die Konfiguration eines Medienstreamgeräts zurück. Synchronous.                                                                                                   |
| [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Gibt den aktuellen Status des angegebenen Open Line-Geräts zurück. Synchronous.                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Legt die Konfiguration des angegebenen Medienstreamgeräts fest. Synchronous.                                                                                      |
| [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Gibt die Statusänderungen an, bei denen die Anwendung benachrichtigt werden muss. Synchronous.                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Ruft eine Geräte-ID ab, die der angegebenen offenen Zeile, Adresse oder dem angegebenen Aufruf zugeordnet ist. Synchronous.                                                                  |
| [**\_TSPI-ZeileGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen. Synchronous.                                                                                |
| [**KONSTRUKTORSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Veranlasst den Anbieter des angegebenen Liniengeräts, ein Dialogfeld anzuzeigen, in dem der Benutzer Parameter konfigurieren kann, die sich auf das Liniengerät bezieht. Synchronous. |
| [**KONSTRUKTORSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Zeigt ein Dialogfeld an, in dem der Benutzer konfigurationsinformationen für ein Liniengerät ändern kann. Synchronous.                                                    |



 

## <a name="addresses"></a>Adressen



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Gibt die Telefoniefunktionen einer Adresse zurück. Synchronous.                           |
| [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Gibt den aktuellen Status einer angegebenen Adresse zurück. Synchronous.                              |
| [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Ruft die Anzahl der Adressbezeichner ab, die in der angegebenen Zeile unterstützt werden.             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Ruft die Adress-ID einer Adresse ab, die in einem alternativen Format angegeben wurde. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Öffnen und Schließen von Line-Geräten



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_TSPI-ZeileOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Öffnet ein angegebenes Liniengerät für die nachfolgende Überwachung und/oder Steuerung der Linie. Synchronous. |
| [**\_TSPI-ZeileSchließen**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Schließt ein angegebenes geöffnetes Zeilengerät. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Aufrufzustände und Ereignisse



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Gibt feste Informationen zu einem Aufruf zurück. Synchronous.                                |
| [**\_TSPI-ZeileGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Gibt vollständige Aufrufstatusinformationen für den angegebenen Aufruf zurück. Synchronous.       |
| [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Legt das anwendungsspezifische Feld der Informationsstruktur eines Aufrufs fest. Synchronous. |



 

## <a name="making-calls"></a>Tätigen von Aufrufen



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Macht einen ausgehenden Aufruf und gibt ein Aufrufhand handle dafür zurück. Asynchron. |
| [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Wählt (Teile einer oder mehrere) wählbare Adressen. Asynchron.         |



 

## <a name="answering-incoming-calls"></a>Beantworten eingehender Anrufe



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|---------------------------------------------|-----------------------------------------|
| [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Beantwortet einen eingehenden Anruf. Asynchron. |



 

## <a name="call-drop-functions"></a>Drop-Funktionen für Aufrufe



|  Funktion                                                         |   BESCHREIBUNG                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Trennt einen Aufruf oder verabsehrt einen aufrufversuch, der in Bearbeitung ist. Asynchron. |



 

 

 
