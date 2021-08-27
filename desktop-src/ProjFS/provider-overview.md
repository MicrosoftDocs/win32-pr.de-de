---
title: Anbieterübersicht
description: Konzeptionelle Übersicht über eine Anbieteranwendung.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6905d6d2d52fd30b8950682c45c9d3bd0fc13281fc0f1d3120cba1b168012d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127960"
---
# <a name="provider-overview"></a>Anbieterübersicht

Der Anbieter ist eine Anwendung im Benutzermodus, die einen Sicherungsdatenspeicher verwaltet und versteht.  Der Anbieter implementiert ProjFS-Rückrufe und verwendet die ProjFS-API, um diesen Datenspeicher in das Dateisystem zu projizieren, wo er dem Benutzer als Dateien und Verzeichnisse angezeigt wird.  Der Sicherungsspeicher des Anbieters kann lokal im System des Benutzers oder remote gespeichert sein.

## <a name="data-projection"></a>Datenprojektion

Der Teil des Dateisystems, den der Anbieter besitzt, in dem seine Daten projiziert werden, befindet sich in einem Verzeichnis, das als "Virtualisierungsstamm" bezeichnet wird.  Wenn der Anbieter mit dem Projizieren seiner Daten beginnen möchte, wird eine "Virtualisierungsinstanz" gestartet. Dabei handelt es sich um ein Objekt, das die Kommunikation zwischen dem Anbieter und ProjFS für den Satz von Dateien und Verzeichnissen verwaltet, die sich unter einem bestimmten Virtualisierungsstamm befinden.  Alle Dateien und Verzeichnisse, die Nachfolger des Virtualisierungsstamms sind und nicht lokal vom Benutzer erstellt wurden, werden vom Anbieter über die ProjFS-API materialisiert.  Diese Elemente beginnen als virtuelle Dateien und Verzeichnisse, was bedeutet, dass sie nicht auf dem lokalen Speichergerät des Benutzers vorhanden sind, sondern von ProjFS in Enumerationsergebnisse eingefügt werden.  Wenn die Elemente geöffnet und gelesen werden, ruft ProjFS Rückrufe auf, die vom Anbieter implementiert werden, um Daten anzufordern, und der Anbieter verwendet ProjFS-APIs, um diese Daten an den lokalen Speicher zu senden, in dem sie für den nachfolgenden Zugriff zwischengespeichert werden.  Wenn sich die Ansicht des Sicherungsdatenspeichers des Benutzers ändern muss, z. B. wenn sich der Inhalt des Datenspeichers geändert hat, kann der Anbieter ProjFS-APIs verwenden, um lokale Elemente zu aktualisieren oder zu löschen, um die neue Ansicht des Datenspeichers widerzuspiegeln.

## <a name="callback-return-codes"></a>Rückrufrückgabecodes

Jeder Rückruf listet eine Reihe möglicher Rückgabewerte auf, die für diesen Rückruf spezifisch sind.  Zusätzlich zu den Rückgabewerten, die für einen bestimmten Rückruf aufgeführt sind, kann ein Rückruf auch bestimmte andere Fehlercodes zurückgeben.  Dies ist die vollständige Liste der Fehlercodes, die ein Rückruf zurückgeben kann:

| Fehlercode                                    | Bedeutung
|-----------------------------------------------|--------
| S_OK                                          | Vorgang erfolgreich
| E_OUTOFMEMORY                                 | Fehler beim Zuordnen des erforderlichen Arbeitsspeichers.
| HRESULT_FROM_WIN32(ERROR_IO_PENDING)          | Der Anbieter möchte den Vorgang zu einem späteren Zeitpunkt abschließen.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Ein an einen Rückruf übergebener Puffer war zu klein.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | Die Datei ist im Sicherungsspeicher des Anbieters nicht vorhanden.
| HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)   | Ein Rückrufargument ist ungültig.  Beispielsweise entspricht eine Enumerations-ID keiner aktiven Enumerationssitzung.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | Der Anbieter möchte verhindern, dass ein Vorgang, z. B. ein Umbenennen oder Löschen, ausgeführt wird.

Rückrufe können auch alle Fehler zurückgeben, die sie möglicherweise von Aufrufen von ProjFS-APIs erhalten.
Wenn ein Rückruf einen Fehlercode zurückgibt, der nicht in der vorherigen Liste enthalten ist oder nicht von einer ProjFS-API stammt, gibt ProjFS ihn als STATUS_INTERNAL_ERROR an das Dateisystem zurück.
