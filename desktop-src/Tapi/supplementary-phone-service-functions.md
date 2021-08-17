---
description: Die Funktionen des ergänzenden Telefondiensts sind in den folgenden Themen nach Kategorie aufgeführt.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Ergänzende Telefon-Dienstfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ee0e32260ac3821fd06e7e8962ab2a6186fb42f1140eb6cd8f705709f2dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861418"
---
# <a name="supplementary-phone-service-functions"></a>Ergänzende Telefon-Dienstfunktionen

Die Funktionen des ergänzenden Telefondiensts sind in den folgenden Themen nach Kategorie aufgeführt. Eine Funktion wird als asynchron [*identifiziert,*](a-tapgloss.md) wenn sie den Abschluss in einer REPLY-Nachricht an die Anwendung andeut. Wenn die Funktion ihr Ergebnis immer sofort an die Anwendung zurückgibt, wird die Funktion als synchron [*betrachtet.*](s-tapgloss.md)

Im Folgenden finden Sie eine funktionale Gruppierung der Funktionen des ergänzenden Telefondiensts:

-   [Schaltflächen](#buttons)
-   [Datenbereiche](#data-areas)
-   [Anzeige](#display)
-   [Hookswitch-Geräte](#hookswitch-devices)
-   [Lamps](#lamps)
-   [Öffnen und Schließen von Telefongeräten](#opening-and-closing-phone-devices)
-   [Telefon initialisieren und herunterfahren](#phone-initialization-and-shutdown)
-   [Telefon und Funktionen](#phone-status-and-capabilities)
-   [Telefon der Versionsaushandlung](#phone-version-negotiation)
-   [Ring](#ring)
-   [Status](#status)

## <a name="phone-initialization-and-shutdown"></a>Telefon Initialisierung und Herunterfahren



| Funktion                                       | Beschreibung                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Initialisiert die TAPI-Telefonabstraktion zur Verwendung durch die aufrufende Anwendung. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Beendet die Verwendung der Phone-Abstraktion von TAPI durch eine Anwendung. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Telefon Versionsaushandlung



| Funktion                                                     | Beschreibung                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Ermöglicht einer Anwendung, eine zu verwendende TAPI-Version auszuhandeln. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Öffnen und Schließen Telefon Geräten



| Funktion                         | Beschreibung                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Öffnet das angegebene Telefongerät und gibt der Anwendung entweder Besitzer- oder Monitorberechtigungen. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Schließt ein angegebenes geöffnetes Telefongerät. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Telefon Status und Funktionen



| Funktion                                       | Beschreibung                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Gibt die Funktionen eines bestimmten Telefongeräts zurück. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Gibt eine Geräte-ID für die angegebene Geräteklasse zurück, die dem angegebenen Telefongerät zugeordnet ist. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Ermöglicht einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Veranlasst den Anbieter des angegebenen Telefongeräts, ein Dialogfeld anzuzeigen, in dem der Benutzer Parameter konfigurieren kann, die sich auf das Telefongerät bezieht. Synchronous. |



 

## <a name="hookswitch-devices"></a>Hookswitch-Geräte



| Funktion                                         | Beschreibung                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Legt den Hookzustand der Hookswitchgeräte eines geöffneten Telefons auf einen angegebenen Modus fest. Asynchron.      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Fragt den Hookswitchmodus eines Hookswitch-Geräts eines geöffneten Telefongeräts ab. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Legt das Volumen des Lautsprechers eines Geräts mit offenem Telefon fest. Asynchron.           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Gibt die Volumeeinstellung des Lautsprechers eines Geräts mit offenem Telefon zurück. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Legt den Gewinn des Mikrofons eines Geräts mit hookswitch eines geöffneten Telefongeräts fest. Asynchron.                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Gibt die Verstärkungseinstellung des Mikrofons eines geöffneten Telefons eines Hookswitchgeräts zurück. Synchronous.              |



 

## <a name="display"></a>Anzeige



| Funktion                                   | Beschreibung                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Schreibt Informationen in die Anzeige eines geöffneten Telefongeräts. Asynchron. |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Gibt den aktuellen Inhalt der Anzeige eines Telefons zurück. Synchronous.          |



 

## <a name="ring"></a>Ring



| Funktion                             | Beschreibung                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Ringt ein offenes Telefongerät gemäß einem bestimmten Ringmodus. Asynchron. |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Gibt den aktuellen Ringmodus eines geöffneten Telefongeräts zurück. Synchronous.    |



 

## <a name="buttons"></a>Schaltflächen



| Funktion                                         | Beschreibung                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Legt die einer Schaltfläche auf einem Telefongerät zugeordneten Informationen fest. Asynchron. |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Gibt Informationen zurück, die einer Schaltfläche auf einem Telefongerät zugeordnet sind. Synchronous.   |



 

## <a name="lamps"></a>Lamps



| Funktion                             | Beschreibung                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Leuchtet eine Lampe auf einem angegebenen geöffneten Telefongerät in einem bestimmten Lampe-Beleuchtungsmodus. Asynchron. |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Gibt den aktuellen Lampemodus der angegebenen Lampe zurück. Synchronous.                           |



 

## <a name="data-areas"></a>Datenbereiche



| Funktion                             | Beschreibung                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Lädt einen Datenpuffer in einen bestimmten Datenbereich auf dem Telefongerät herunter. Asynchron.      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Lädt den Inhalt eines bestimmten Datenbereichs auf dem Telefongerät in einen Puffer hoch. Synchronous. |



 

## <a name="status"></a>Status



| Funktion                                                 | Beschreibung                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden soll. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Gibt die Statusänderungen zurück, für die die Anwendung benachrichtigt werden soll. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Gibt den vollständigen Status eines geöffneten Telefongeräts zurück. Synchronous.                         |



 

 

 



