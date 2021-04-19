---
title: Funktionen zur Verhinderung von Endpunktdatenverlust
description: Funktionen, die von der Funktion zur Verhinderung von Datenverlust des Endpunkts verwendet werden.
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f8713a6a6051bf477b4f9c7f6f8a7430abf70a52
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495589"
---
# <a name="endpoint-data-loss-prevention-functions"></a>Funktionen zur Verhinderung von Endpunktdatenverlust

Funktionen, die von der Funktion zur Verhinderung von Datenverlust des Endpunkts verwendet werden.



| Functions                                                       | BESCHREIBUNG                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Stellt dem System Informationen zu einem Dokument bereit, bevor der Vorgang zum Schließen des Dokuments initiiert wird.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Stellt dem System Informationen zu einem Dokument bereit, bevor der Vorgang zum Schließen des Dokuments initiiert wird.                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Stellt dem System Informationen zu einem Dokument bereit, wenn ein Ablageziel eingegeben wird.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Ruft die Version der DLP-API (Data Loss Prevention) des Endpunkts auf dem aktuellen Gerät ab.                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von DLP-Vorgängen (Endpoint Data Loss Prevention).                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Bestimmt, ob die App die Daten aus der Zwischenablage des Systems abrufen muss, anstatt sie aus dem internen Cache zu entfernen.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Stellt dem System Informationen zu einem Dokument bereit, wenn ein Ablageziel beendet wird.                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Kopiervorgang in die Zwischenablage abgeschlossen wurde.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Stellt dem System Nach Abschluss eines Drag &amp; Drop-Vorgangs Informationen zu einem Dokument zur Verfügung.  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Öffnen-Vorgang abgeschlossen wurde.                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Öffnen-Vorgang abgeschlossen wurde.                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang abgeschlossen wurde.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Vorgang zum Speichern unter abgeschlossen wurde.                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang gestartet wurde.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Stellt dem System Nach Abschluss eines Stash-Zwischenablage-Vorgangs Statusinformationen zur Verfügung.                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Drag Drop-Vorgang initiiert wird.  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor der Öffnungsvorgang initiiert wird.  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor der Öffnungsvorgang initiiert wird.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor ein Einfügen aus der Zwischenablage initiiert wird.  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor ein Druckvorgang initiiert wird.  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Stellt dem System Informationen zu einem Dokument bereit, bevor ein Save-as-Vorgang initiiert wird.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Benachrichtigt das System, bevor ein Stash-Zwischenablagevorgang initiiert wird.                                  |