---
description: Um die Übertragung von Anwendungsdateien zu ermöglichen, verwaltet COMREPL automatisch Sätze von Dateisystemordnern auf der Quelle und dem Ziel. Diese COMREPL-Ordner befinden sich alle in %systemdir% \\ \\ com-Replikation.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Dateiverwaltung (Komponentendienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685287e783dc5ae45d564897a37733568cc150d9af43322d5f435100e8f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307315"
---
# <a name="file-management"></a>Dateiverwaltung

Um die Übertragung von Anwendungsdateien zu ermöglichen, verwaltet COMREPL automatisch Sätze von Dateisystemordnern auf der Quelle und dem Ziel. Diese COMREPL-Ordner befinden sich alle in %systemdir% \\ \\ com-Replikation.

## <a name="source-folders"></a>Quellordner



| Ordner                   | Zweck                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Anwendungen, die während der Vorbereitungsphase exportiert werden, werden hier gespeichert.<br/> Dieser Ordner wird jedes Mal überschrieben, wenn die Vorbereitungsphase für einen bestimmten Quellcomputer ausgeführt wird. Dieser Ordner wird nie explizit gelöscht, sodass die Replikation auf Ziele jederzeit nach der Vorbereitung der Quelle stattfinden kann.<br/> Jede Anwendung wird in einem eigenen Unterordner namens <appName> + <appID> gespeichert.<br/> |



 

## <a name="target-folders"></a>Zielordner



| Ordner                    | Zweck                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | In der Kopierphase werden alle Dateien und Unterordner aus ReplicaSource in der Quelle in ReplicaNew auf dem Ziel kopiert. Alle vorherigen Inhalte von ReplicaNew werden jedes Mal gelöscht, wenn die Kopierphase für ein bestimmtes Ziel ausgeführt wird.<br/> Dieser Ordner ist nur vorhanden, während der Replikationsprozess ausgeführt wird. (Siehe ReplicaCurrent.)<br/>           |
| ReplicaCurrent<br/> | Die replizierten Anwendungen, die derzeit auf dem Ziel installiert sind, werden hier gespeichert.<br/> Wenn die Installationsphase gestartet wird, wird der Ordner ReplicaNew in ReplicaCurrent umbenannt. Wenn ein ReplicaCurrent-Ordner vorhanden ist, wird er in ReplicaOld umbenannt. Wenn ein ReplicaOld-Ordner vorhanden ist, wird sein Inhalt gelöscht.<br/> |
| ReplicaOld<br/>     | Speichert die Anwendungsdateien, die während der nächsten bis zur letzten Replikation installiert wurden. Diese Dateien werden nur zu Sicherungszwecken gespeichert.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Replikationsphasen](replication-phases.md)
</dt> <dt>

[Verwenden von COMREPL](using-comrepl.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 




