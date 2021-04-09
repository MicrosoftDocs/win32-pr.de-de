---
description: Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Grundlegende Telefoniefunktionen von TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868599"
---
# <a name="tspi-basic-telephony-functions"></a>Grundlegende Telefoniefunktionen von TSPI

Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren. Im folgenden finden Sie eine Liste dieser Funktionen nach Kategorie. Eine Funktion wird als *asynchron* identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt. Wenn die Funktion das Ergebnis immer sofort zurückgibt, wird die Funktion als *synchron* betrachtet.

-   [Adresses](#addresses)
-   [Beantworten eingehender Anrufe](#answering-incoming-calls)
-   [Drop Functions-Aufrufe](#call-drop-functions)
-   [Aufrufe von Zuständen und Ereignissen](#call-states-and-events)
-   [Zeilen Status und-Funktionen](#line-status-and-capabilities)
-   [Aushandlung der Zeilen Version](#line-version-negotiation)
-   [Aufrufen](#making-calls)
-   [Öffnen und Schließen von Linien Geräten](#opening-and-closing-line-devices)
-   [Aushandlung der Telefon Version](#phone-version-negotiation)
-   [TSP-Initialisierung und-Herunterfahren](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>TSP-Initialisierung und-Herunterfahren



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**Tuispi \_ providerinstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Installiert einen TSP. Synchronous.                              |
| [**TSPI \_ providerinstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Installiert den TSP. Veraltet mit Version 2,0. Synchronous. |
| [**TSPI \_ providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Initialisiert den TSP. Synchronous.                         |
| [**TSPI \_ providershutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Fährt den Dienstanbieter herunter.                          |
| [**Tuispi \_ providerremove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Entfernt einen TSP. Synchronous.                               |
| [**TSPI \_ providerremove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Entfernt einen TSP. Veraltet mit Version 2,0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Aushandlung der Telefon Version



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phonenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Gibt die höchste SPI-Version zurück, unter der der Dienstanbieter für dieses Gerät arbeiten kann. |



 

## <a name="line-version-negotiation"></a>Aushandlung der Zeilen Version



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TSPI \_ linenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Ermöglicht es einer Anwendung, eine TSPI-Version zu aushandeln, die mit einem bestimmten liniengerät verwendet werden soll. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Zeilen Status und-Funktionen



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ linegetdevcaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Gibt die Funktionen eines angegebenen Zeilen Geräts zurück. Synchronous.                                                                                                  |
| [**TSPI \_ linegetdevconfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Gibt die Konfiguration eines Medienstrom Geräts zurück. Synchronous.                                                                                                   |
| [**TSPI \_ linegetlinedevstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Gibt den aktuellen Status des angegebenen Open-Line-Geräts zurück. Synchronous.                                                                                         |
| [**TSPI \_ linesetdevconfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Legt die Konfiguration des angegebenen Medienstrom Geräts fest. Synchronous.                                                                                      |
| [**TSPI- \_ linesetstatus-Meldungen**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden muss. Synchronous.                                                                      |
| [**TSPI- \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Ruft eine Geräte-ID ab, die der angegebenen öffnenden Zeile, Adresse oder dem angegebenen-Befehl zugeordnet ist. Synchronous.                                                                  |
| [**TSPI- \_ linegeticon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen. Synchronous.                                                                                |
| [**Tuispi \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Bewirkt, dass der Anbieter des angegebenen Zeilen Geräts ein Dialogfeld anzeigt, das es dem Benutzer ermöglicht, Parameter im Zusammenhang mit dem liniengerät zu konfigurieren. Synchronous. |
| [**Tuispi \_ lineconfigdialogedit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Zeigt ein Dialogfeld an, in dem der Benutzer Konfigurationsinformationen für ein liniengerät ändern kann. Synchronous.                                                    |



 

## <a name="addresses"></a>Adressen



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ linegetaddresscaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Gibt die Telefoniefunktionen einer Adresse zurück. Synchronous.                           |
| [**TSPI \_ linegetaddressstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Gibt den aktuellen Status einer angegebenen Adresse zurück. Synchronous.                              |
| [**TSPI \_ linegetnumaddressids**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Ruft die Anzahl der auf der angegebene Zeile unterstützten Adress Bezeichner ab.             |
| [**TSPI \_ linegetadressssid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Ruft die Adress-ID einer Adresse ab, die mit einem alternativen Format angegeben wird. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Öffnen und Schließen von Linien Geräten



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**TSPI ( \_ lineOpen)**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Öffnet ein angegebenes Zeilen Gerät zum Bereitstellen der nachfolgenden Überwachung und/oder Steuerung der Zeile. Synchronous. |
| [**TSPI- \_ lineclose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Schließt ein angegebenes geöffnetes Zeilen Gerät. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Aufrufe von Zuständen und Ereignissen



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**TSPI \_ linegetcallinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Gibt fixierte Informationen zu einem-Befehl zurück. Synchronous.                                |
| [**TSPI \_ linegetcallstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Gibt die Statusinformationen zum Abschluss des angegebenen Aufrufes zurück. Synchronous.       |
| [**TSPI \_ linesetappspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Legt das anwendungsspezifische Feld der Informationsstruktur eines Aufrufes fest. Synchronous. |



 

## <a name="making-calls"></a>Aufrufen



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Führt einen ausgehenden-Rückruf aus und gibt ein-Rückruf handle dafür zurück. Asynchron. |
| [**TSPI- \_ linedial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Dials (Teile von einer oder mehreren), die als nicht zulässig sind. Asynchron.         |



 

## <a name="answering-incoming-calls"></a>Beantworten eingehender Anrufe



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [**TSPI- \_ lineanswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Beantwortet einen eingehenden-Befehl. Asynchron. |



 

## <a name="call-drop-functions"></a>Drop Functions-Aufrufe



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**TSPI- \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Trennt einen-Befehl oder bricht einen aufzurufenden Versuch ab. Asynchron. |



 

 

 
