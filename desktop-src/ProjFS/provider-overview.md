---
title: Übersicht über den Anbieter
description: Konzeptionelle Übersicht über eine Anbieter Anwendung.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 89b49096b7b68a723b52b4eb998c446661b7d3c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474799"
---
# <a name="provider-overview"></a>Übersicht über den Anbieter

Der Anbieter ist eine Benutzermodusanwendung, die einen Sicherungsdaten Speicher verwaltet und versteht.  Der Anbieter implementiert projfs-Rückrufe und verwendet die projfs-API, um diesen Datenspeicher in das Dateisystem zu projizieren, in dem der Benutzer als Dateien und Verzeichnisse angezeigt wird.  Der Sicherungs Speicher des Anbieters ist möglicherweise lokal im System des Benutzers, oder er befindet sich möglicherweise Remote.

## <a name="data-projection"></a>Datenprojektion

Der Teil des Dateisystems, dem der Anbieter gehört, dessen Daten projiziert werden, befindet sich in einem Verzeichnis namens "virtualisierungsroot".  Wenn der Anbieter seine Daten projizieren möchte, startet er eine "virtualisierungsinstanz", bei der es sich um ein Objekt handelt, das die Kommunikation zwischen dem Anbieter und projfs für die Gruppe von Dateien und Verzeichnissen verwaltet, die sich unter einem bestimmten virtualisierungsstamm befinden.  Alle Dateien und Verzeichnisse, die Nachfolger des virtualisierungsstamms sind, die nicht lokal vom Benutzer erstellt wurden, werden vom Anbieter über die projfs-API materialisiert.  Diese Elemente werden als virtuelle Dateien und Verzeichnisse gestartet, was bedeutet, dass Sie nicht auf dem lokalen Speichergerät des Benutzers vorhanden sind, sondern in die enumerationsergebnisse von projfs eingefügt werden.  Wenn die Elemente geöffnet und gelesen werden, ruft projfs Rückrufe auf, die vom Anbieter für die Anforderung von Daten implementiert werden, und der Anbieter verwendet projfs-APIs, um diese Daten an den lokalen Speicher zu senden, in dem Sie für den nachfolgenden Zugriff zwischengespeichert wird.  Wenn sich der Datenspeicher des Benutzers ändern muss, beispielsweise, wenn sich der Inhalt des Datenspeicher geändert hat, kann der Anbieter die projfs-APIs verwenden, um lokale Elemente zu aktualisieren oder zu löschen, um die neue Ansicht des Datenspeicher widerzuspiegeln.

## <a name="callback-return-codes"></a>Rückruf Rückgabecodes

Jeder Rückruf listet eine Reihe möglicher Rückgabewerte auf, die für diesen Rückruf spezifisch sind.  Zusätzlich zu den Rückgabe Werten, die für einen bestimmten Rückruf aufgelistet werden, kann ein Rückruf auch bestimmte andere Fehlercodes zurückgeben.  Dies ist die komplette Liste der Fehlercodes, die ein Rückruf zurückgeben kann:

| Fehlercode                                    | Bedeutung
|-----------------------------------------------|--------
| S_OK                                          | Vorgang erfolgreich
| E_OUTOFMEMORY                                 | Der erforderliche Arbeitsspeicher konnte nicht belegt werden.
| HRESULT_FROM_WIN32 (ERROR_IO_PENDING)          | Der Anbieter möchte den Vorgang zu einem späteren Zeitpunkt durchführen.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Ein Puffer, der an einen Rückruf übermittelt wurde, war zu klein.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | Die Datei ist nicht im Sicherungs Speicher des Anbieters vorhanden.
| HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)   | Ein Rückruf Argument ist ungültig.  Beispielsweise entspricht eine enumerationskennung keiner aktiven enumerationssitzung.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | Der Anbieter möchte verhindern, dass ein Vorgang (z. b. ein umbenennen oder löschen) stattfindet.

Rückrufe können auch Fehler zurückgeben, die von Aufrufen von projfs-APIs empfangen werden können.
Wenn ein Rückruf einen Fehlercode zurückgibt, der nicht in der vorangehenden Liste enthalten ist oder der nicht von einer projfs-API stammt, wird er von projfs als STATUS_INTERNAL_ERROR an das Dateisystem zurückgegeben.
