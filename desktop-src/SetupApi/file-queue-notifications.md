---
description: Die folgenden Benachrichtigungen werden bei Datei Warteschlangen verwendet. Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter Benachrichtigungen.
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: Datei Warteschlangen Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b674dee015c4c9408ff5dc853d5d3b2412e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042596"
---
# <a name="file-queue-notifications"></a>Datei Warteschlangen Benachrichtigungen

Die folgenden Benachrichtigungen werden bei Datei Warteschlangen verwendet. Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter [Benachrichtigungen](notifications.md).



| Benachrichtigung                                                      | Beschreibung                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**spfilenotify \_ copyError**](spfilenotify-copyerror.md)         | Fehler während eines Datei Kopiervorgangs.                                                  |
| [**deleteerror für spfilenotify \_**](spfilenotify-deleteerror.md)     | Fehler beim Löschen der Datei.                                                 |
| [**spfilenotify- \_ endkopie**](spfilenotify-endcopy.md)             | Ein Datei Kopiervorgang wurde beendet.                                                                 |
| [**spfilenotify- \_ enddelete**](spfilenotify-enddelete.md)         | Ein Datei Löschvorgang wurde beendet.                                                                |
| [**spfilenotify- \_ endwarteschlange**](spfilenotify-endqueue.md)           | Der Commit der Warteschlange ist abgeschlossen.                                                                  |
| [**spfilenotify \_ endrename**](spfilenotify-endrename.md)         | Ein Vorgang zum Umbenennen der Datei wurde beendet.                                                                  |
| [**spfilenotifident \_ endsubqueue**](spfilenotify-endsubqueue.md)     | Eine unter Warteschlange (kopieren, umbenennen oder löschen) wurde beendet.                                               |
| [**\_spfilenotififileopverzögert**](spfilenotify-fileopdelayed.md) | Die Datei wurde verwendet, und der aktuelle Vorgang wurde verzögert, bis das System neu gestartet wird.       |
| [**spfilenotify nicht übereinstimmende \_**](spfilenotify-langmismatch.md)   | Die Sprache des aktuellen Vorgangs entspricht nicht der Systemsprache.                           |
| [**spfilenotify \_ needmedia**](spfilenotify-needmedia.md)         | Es wird ein neues Quell Medium benötigt.                                                                         |
| [**spfilenotify \_ queuescan**](spfilenotify-queuescan.md)         | Ein Knoten in der Datei Warteschlange wurde gescannt. (Nur [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ) |
| [**spfilenotify \_ renameerror**](spfilenotify-renameerror.md)     | Fehler während eines Datei Umbenennungs Vorgangs.                                                 |
| [**spfilenotify \_ StartCopy**](spfilenotify-startcopy.md)         | Ein Datei Kopiervorgang wurde gestartet.                                                                  |
| [**spfilenotify \_ startdelete**](spfilenotify-startdelete.md)     | Ein Datei Löschvorgang wurde gestartet.                                                                |
| [**spfilenotify \_ startqueue**](spfilenotify-startqueue.md)       | Der Commit der Warteschlange wurde gestartet.                                                                    |
| [**spfilenotify \_ startrename**](spfilenotify-startrename.md)     | Ein Vorgang zum Umbenennen von Dateien wurde gestartet.                                                                |
| [**spfilenotify \_ startsubqueue**](spfilenotify-startsubqueue.md) | Eine unter Warteschlange (kopieren, umbenennen oder löschen) wurde gestartet.                                             |
| [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md)   | Eine Kopie der angegebenen Datei ist bereits auf dem Ziel vorhanden.                                          |
| [**spfilenotify \_ targetneuere**](spfilenotify-targetnewer.md)     | Eine neuere Version der angegebenen Datei ist auf dem Ziel vorhanden.                                         |



 

 

 



