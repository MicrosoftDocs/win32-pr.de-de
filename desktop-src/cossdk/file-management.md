---
description: Um die Übertragung von Anwendungs Dateien zu ermöglichen, verwaltet Comrepl automatisch Sätze von Dateisystem Ordnern auf Quelle und Ziel. Diese Comrepl-Ordner basieren alle auf der% System dir% \\ com- \\ Replikation.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Dateiverwaltung (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523427"
---
# <a name="file-management"></a>Dateiverwaltung

Um die Übertragung von Anwendungs Dateien zu ermöglichen, verwaltet Comrepl automatisch Sätze von Dateisystem Ordnern auf Quelle und Ziel. Diese Comrepl-Ordner basieren alle auf der% System dir% \\ com- \\ Replikation.

## <a name="source-folders"></a>Quellordner



| Ordner                   | Zweck                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Replicasource<br/> | Anwendungen, die während der Vorbereitungsphase exportiert werden, werden hier gespeichert.<br/> Dieser Ordner wird jedes Mal überschrieben, wenn die Vorbereitungsphase für einen bestimmten Quellcomputer ausgeführt wird. Dieser Ordner wird nie explizit gelöscht, sodass die Replikation an Ziele jederzeit erfolgen kann, nachdem die Quelle vorbereitet wurde.<br/> Jede Anwendung wird in einem eigenen Unterordner mit dem Namen gespeichert <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Zielordner



| Ordner                    | Zweck                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Replikanew<br/>     | In der Kopier Phase werden alle Dateien und Unterordner von replicasource auf der Quelle in replicanew auf dem Ziel kopiert. Alle vorherigen Inhalte der replicanew werden immer dann gelöscht, wenn die Kopier Phase für ein bestimmtes Ziel ausgeführt wird.<br/> Dieser Ordner ist nur vorhanden, während der Replikationsprozess ausgeführt wird. (Siehe replicacurrent.)<br/>           |
| Replicacurrent<br/> | Die replizierten Anwendungen, die zurzeit auf dem Ziel installiert sind, werden hier gespeichert.<br/> Wenn die Installationsphase gestartet wird, wird der Ordner "replicanew" in "replicacurrent" umbenannt. Wenn ein vorhandener replicacurrent-Ordner vorhanden ist, wird er in replicaold umbenannt. Wenn ein vorhandener replicaold-Ordner vorhanden ist, wird der zugehörige Inhalt gelöscht.<br/> |
| Replicaold<br/>     | Speichert die Anwendungs Dateien, die während der nächsten Replikation installiert werden. Diese Dateien werden nur zu Sicherungszwecken gespeichert.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Replikations Phasen](replication-phases.md)
</dt> <dt>

[Verwenden von Comrepl](using-comrepl.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 




