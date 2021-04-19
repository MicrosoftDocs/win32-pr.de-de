---
description: Die grundlegenden Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Grundlegende telefoniedienstreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348289"
---
# <a name="basic-telephony-services-reference"></a>Grundlegende telefoniedienstreferenz

Die grundlegenden Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet. Eine Funktion wird als [*asynchron*](a-tapgloss.md) identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt. Wenn die Funktion das Ergebnis immer sofort an die Anwendung zurückgibt, gilt die Funktion als [*synchron*](s-tapgloss.md).

Im folgenden finden Sie eine funktionale Gruppierung der grundlegenden telefoniedienstfunktionen:

-   [Adressformate](#address-formats)
-   [Adresses](#addresses)
-   [Beantworten eingehender Anrufe](#answering-incoming-calls)
-   [Drop Functions-Aufrufe](#call-drop-functions)
-   [Bearbeitung von anrufhandles](#call-handle-manipulation)
-   [Berechtigungs Steuerelement anrufen](#call-privilege-control)
-   [Aufrufe von Zuständen und Ereignissen](#call-states-and-events)
-   [Zeilen Status und-Funktionen](#line-status-and-capabilities)
-   [Aushandlung der Zeilen Version](#line-version-negotiation)
-   [Standort-und Land/Region-Informationen](#location-and-countryregion-information)
-   [Aufrufen](#making-calls)
-   [Öffnen und Schließen von Linien Geräten](#opening-and-closing-line-devices)
-   [Empfänger Dienste anfordern](#request-recipient-services)
-   [TAPI-Initialisierung und-Herunterfahren](#tapi-initialization-and-shutdown)
-   [Unterstützung für Maut Sparer](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a>TAPI-Initialisierung und-Herunterfahren



| Funktion                                     | BESCHREIBUNG                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | Initialisiert die TAPI-Zeilen Abstraktion, die von der Aufruf Anwendung verwendet werden soll. Synchronous. |
| [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | Schaltet die Verwendung der TAPI-Zeilen Abstraktion durch die Anwendung herunter. Synchronous.               |



 

## <a name="line-version-negotiation"></a>Aushandlung der Zeilen Version



| Funktion                                                   | BESCHREIBUNG                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | Ermöglicht es einer Anwendung, eine TAPI-Version für die Verwendung von auszuhandeln. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Zeilen Status und-Funktionen



| Funktion                                               | BESCHREIBUNG                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | Gibt die Funktionen eines angegebenen Zeilen Geräts zurück. Synchronous.                                                                                                  |
| [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | Gibt die Konfiguration eines Medienstrom Geräts zurück. Synchronous.                                                                                                   |
| [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | Gibt den aktuellen Status des angegebenen Open-Line-Geräts zurück. Synchronous.                                                                                         |
| [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | Legt die Konfiguration des angegebenen Medienstrom Geräts fest. Synchronous.                                                                                      |
| [**linesetstatus-Meldungen**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden muss. Synchronous.                                                                      |
| [**linegetstatus Messages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | Gibt die aktuellen Zeilen-und Adress Status Meldungs Einstellungen der Anwendung zurück. Synchronous.                                                                       |
| [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | Ruft eine Geräte-ID ab, die der angegebenen öffnenden Zeile, Adresse oder dem angegebenen-Befehl zugeordnet ist. Synchronous.                                                                  |
| [**linegeticon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen. Synchronous.                                                                                |
| [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | Bewirkt, dass der Anbieter des angegebenen Zeilen Geräts ein Dialogfeld anzeigt, das es dem Benutzer ermöglicht, Parameter im Zusammenhang mit dem liniengerät zu konfigurieren. Synchronous. |
| [**lineconfigdialogedit**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | Zeigt ein Dialogfeld an, in dem der Benutzer Konfigurationsinformationen für ein liniengerät ändern kann. Synchronous.                                                    |



 

## <a name="addresses"></a>Adressen



| Funktion                                             | BESCHREIBUNG                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | Gibt die Telefoniefunktionen einer Adresse zurück. Synchronous.                           |
| [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | Gibt den aktuellen Status einer angegebenen Adresse zurück. Synchronous.                              |
| [**linegetadressssid**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | Ruft die Adress-ID einer Adresse ab, die mit einem alternativen Format angegeben wird. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Öffnen und Schließen von Linien Geräten



| Funktion                       | BESCHREIBUNG                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | Öffnet ein angegebenes Zeilen Gerät zum Bereitstellen der nachfolgenden Überwachung und/oder Steuerung der Zeile. Synchronous. |
| [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) | Schließt ein angegebenes geöffnetes Zeilen Gerät. Synchronous.                                                        |



 

## <a name="address-formats"></a>Adressformate



| Funktion                                                 | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | Übersetzt eine Adresse im kanonischen Format und eine Adresse im ddbaren Format. Synchronous. |
| [**linesetcurrentlocation**](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | Legt den Speicherort fest, der als Kontext für die Adressübersetzung verwendet wird. Synchronous.                       |
| [**linesettolllist**](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | Bearbeitet die Maut Liste. Synchronous.                                                           |
| [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | Gibt Adress Übersetzungsfunktionen zurück. Synchronous.                                            |



 

## <a name="call-states-and-events"></a>Aufrufe von Zuständen und Ereignissen



| Funktion                                         | BESCHREIBUNG                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | Gibt fixierte Informationen zu einem-Befehl zurück. Synchronous.                                |
| [**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | Gibt die Statusinformationen zum Abschluss des angegebenen Aufrufes zurück. Synchronous.       |
| [**linesetappspecific**](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | Legt das anwendungsspezifische Feld der Informationsstruktur eines Aufrufes fest. Synchronous. |



 

## <a name="making-calls"></a>Aufrufen



| Funktion                             | BESCHREIBUNG                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | Führt einen ausgehenden-Rückruf aus und gibt ein-Rückruf handle dafür zurück. Asynchron. |
| [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial)         | Dials (Teile von einer oder mehreren), die als nicht zulässig sind. Asynchron.         |



 

## <a name="answering-incoming-calls"></a>Beantworten eingehender Anrufe



| Funktion                         | BESCHREIBUNG                             |
|----------------------------------|-----------------------------------------|
| [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | Beantwortet einen eingehenden-Befehl. Asynchron. |



 

## <a name="toll-saver-support"></a>Unterstützung für Maut Sparer



| Funktion                                   | BESCHREIBUNG                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**linesetnumrings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | Gibt die Anzahl der Ringe an, nach denen eingehende Aufrufe beantwortet werden sollen. Synchronous.                   |
| [**linegetnumrings**](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | Gibt die Mindestanzahl der mit [**linesetnumrings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings)angeforderten Ringe zurück. Synchronous. |



 

## <a name="call-privilege-control"></a>Berechtigungs Steuerelement anrufen



| Funktion                                             | BESCHREIBUNG                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**linesetcallprivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | Legt die Berechtigung der Anwendung auf das angegebene Privileg fest. Synchronous. |



 

## <a name="call-drop-functions"></a>Drop Functions-Aufrufe



| Funktion                                         | BESCHREIBUNG                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | Trennt einen-Befehl oder bricht einen aufzurufenden Versuch ab. Asynchron. |
| [**linedezugewiesene eCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | Hebt die Zuordnung des angegebenen-Rückruf Handles auf. Synchronous.                       |



 

## <a name="call-handle-manipulation"></a>Bearbeitung von anrufhandles



| Funktion                                                   | BESCHREIBUNG                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**linehandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | Übergibt den Besitz von Anrufen und/oder ändert die Berechtigungen einer Anwendung in einen-Befehl. Synchronous.                                    |
| [**linegetnewcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | Gibt Aufruf Handles zum Aufrufen einer angegebenen Zeile oder Adresse zurück, für die die Anwendung noch keine Handles hat. Synchronous. |
| [**lineget-frelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | Gibt eine Liste von aufrufhandles zurück, die Teil desselben Konferenz Aufrufes sind wie der als Parameter angegebene-Befehl. Synchronous.    |



 

## <a name="location-and-countryregion-information"></a>Standort-und Land/Region-Informationen



| Funktion                                           | BESCHREIBUNG                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**linetranslatedialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | Zeigt ein Dialogfeld an, in dem der Benutzer den Speicherort und die Aufruf Karteninformationen ändern kann. Synchronous. |
| [**linegetcountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | Ruft Wähl Regeln und andere Informationen zu einem bestimmten Land oder einer bestimmten Region ab. Synchronous.              |



 

## <a name="request-recipient-services"></a>Empfänger Dienste anfordern

Die folgenden zwei Funktionen werden nur zur Unterstützung von unterstützten Telefoniefunktionen verwendet.



| Funktion                                                             | BESCHREIBUNG                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineregisterrequestrecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | Registriert oder hebt die Registrierung der Anwendung als Anforderungs Empfänger für den angegebenen Anforderungs Modus auf. Synchronous. |
| [**linegetrequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | Ruft die nächste Anforderung aus der telefoniebibliothek für dynamische links ab. Synchronous.                                  |



 

 

 



