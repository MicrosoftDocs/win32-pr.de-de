---
description: Die zusätzlichen Telefondienst Funktionen sind in den folgenden Themen nach Kategorie aufgelistet.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Zusätzliche Funktionen für den Telefondienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367931"
---
# <a name="supplementary-phone-service-functions"></a>Zusätzliche Funktionen für den Telefondienst

Die zusätzlichen Telefondienst Funktionen sind in den folgenden Themen nach Kategorie aufgelistet. Eine Funktion wird als [*asynchron*](a-tapgloss.md) identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt. Wenn die Funktion das Ergebnis immer sofort an die Anwendung zurückgibt, gilt die Funktion als [*synchron*](s-tapgloss.md).

Im folgenden finden Sie eine funktionale Gruppierung der ergänzenden Phone Service-Funktionen:

-   [Schaltflächen](#buttons)
-   [Datenbereiche](#data-areas)
-   [Anzeige](#display)
-   [Gerätewechsel Geräte](#hookswitch-devices)
-   [Aufleuchten](#lamps)
-   [Öffnen und Schließen von Telefongeräten](#opening-and-closing-phone-devices)
-   [Telefon Initialisierung und Herunterfahren](#phone-initialization-and-shutdown)
-   [Telefonstatus und-Funktionen](#phone-status-and-capabilities)
-   [Aushandlung der Telefon Version](#phone-version-negotiation)
-   [Mandel](#ring)
-   [Status](#status)

## <a name="phone-initialization-and-shutdown"></a>Telefon Initialisierung und Herunterfahren



| Funktion                                       | BESCHREIBUNG                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Initialisiert die TAPI-telefonabstraktion zur Verwendung durch die Aufruf Anwendung. Synchronous. |
| [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Fährt die Verwendung der TAPI-Telefon Abstraktion für eine Anwendung herunter. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Aushandlung der Telefon Version



| Funktion                                                     | BESCHREIBUNG                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Ermöglicht es einer Anwendung, eine TAPI-Version für die Verwendung von auszuhandeln. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Öffnen und Schließen von Telefongeräten



| Funktion                         | BESCHREIBUNG                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Öffnet das angegebene Telefongerät und erteilt der Anwendung entweder Besitzer-oder Monitor Berechtigungen. Synchronous. |
| [**phoneclose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Schließt ein angegebenes geöffnetes Telefongerät. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Telefon Status und-Funktionen



| Funktion                                       | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Gibt die Funktionen eines angegebenen Telefon Geräts zurück. Synchronous.                                                                                                   |
| [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Gibt eine Geräte-ID für die angegebene Geräteklasse zurück, die dem angegebenen Telefongerät zugeordnet ist. Synchronous.                                                          |
| [**phonegeticon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen. Synchronous.                                                                                  |
| [**phoneconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Bewirkt, dass der Anbieter des angegebenen Telefon Geräts ein Dialogfeld anzeigt, das es dem Benutzer ermöglicht, Parameter im Zusammenhang mit dem Telefongerät zu konfigurieren. Synchronous. |



 

## <a name="hookswitch-devices"></a>Gerätewechsel Geräte



| Funktion                                         | BESCHREIBUNG                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Legt den Hook-Zustand der geöffnenden Geräte eines geöffneten Telefons auf einen angegebenen Modus fest. Asynchron.      |
| [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Fragt den Modus "geokswitch" eines geöffnenden Telefon Geräts ab. Synchronous.          |
| [**phonesetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Legt das Volume eines geöffnenden Telefon Geräts für einen Hostgerät fest. Asynchron.           |
| [**phonegetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Gibt die volumeeinstellung eines Sprechers eines geöffnenden Telefons für ein geöffnetes Telefongerät zurück. Synchronous. |
| [**phonesetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Legt den Gewinn der MIC eines geöffnenden Telefon Geräts für ein geöffnetes Gerät fest. Asynchron.                 |
| [**phonegetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Gibt die ergriffseinstellung eines geöffnenden Telefons eines geöffnenden Telefons für ein geöffnetes Gerät zurück. Synchronous.              |



 

## <a name="display"></a>Anzeige



| Funktion                                   | BESCHREIBUNG                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phonesetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Schreibt Informationen in die Anzeige eines geöffneten Telefon Geräts. Asynchron. |
| [**phonegetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Gibt den aktuellen Inhalt der Anzeige eines Telefons zurück. Synchronous.          |



 

## <a name="ring"></a>Ring



| Funktion                             | BESCHREIBUNG                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phonesetring**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Beendet ein geöffnetes Telefongerät entsprechend einem bestimmten Ring Modus. Asynchron. |
| [**phonegetralling**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Gibt den aktuellen Ring Modus eines geöffneten Telefon Geräts zurück. Synchronous.    |



 

## <a name="buttons"></a>Schaltflächen



| Funktion                                         | BESCHREIBUNG                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phonesetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Legt die mit einer Schaltfläche auf einem Telefongerät verknüpften Informationen fest. Asynchron. |
| [**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Gibt Informationen zurück, die mit einer Schaltfläche auf einem Telefongerät verknüpft sind. Synchronous.   |



 

## <a name="lamps"></a>Aufleuchten



| Funktion                             | BESCHREIBUNG                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phonesetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Leuchtet eine LAMP auf einem angegebenen geöffneten Telefongerät in einem bestimmten Lamp-Beleuchtungs Modus. Asynchron. |
| [**phonegetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Gibt den aktuellen Lamp-Modus der angegebenen Lamp zurück. Synchronous.                           |



 

## <a name="data-areas"></a>Datenbereiche



| Funktion                             | BESCHREIBUNG                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phonesetdata**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Lädt einen Datenpuffer in einen bestimmten Datenbereich auf dem Telefongerät herunter. Asynchron.      |
| [**phonegetdata**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Lädt den Inhalt eines bestimmten Datenbereichs auf dem Telefongerät in einen Puffer hoch. Synchronous. |



 

## <a name="status"></a>Status



| Funktion                                                 | BESCHREIBUNG                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phonesetstatus-Meldungen**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden soll. Synchronous. |
| [**phonegetstatus Messages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Gibt die Statusänderungen zurück, für die die Anwendung benachrichtigt werden soll. Synchronous.   |
| [**phonegetstatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Gibt den gesamten Status eines geöffneten Telefon Geräts zurück. Synchronous.                         |



 

 

 



