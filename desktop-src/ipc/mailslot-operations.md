---
description: Beschreibungen der Funktionen, die beim Arbeiten mit Mailslots, Clients und Servern verwendet werden sollen.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Mailslot-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fefce55c70971f5d611c41d473180897706bc04960509818cb0d092c7f83825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829500"
---
# <a name="mailslot-operations"></a>Mailslot-Vorgänge

Bei der Arbeit mit Mailslots sollten Clients und Server nur die in den folgenden Tabellen beschriebenen Funktionen verwenden. Verwenden Sie keine anderen Funktionen, auch wenn sie Dateihandles oder Dateinamen als Parameter akzeptieren, da sie nicht für die Arbeit mit Mailslots konzipiert sind.

## <a name="mailslot-server-functions"></a>Maillot-Serverfunktionen

Maillot-Server verwenden ausschließlich drei Funktionen, wie in der folgenden Tabelle gezeigt.



| Funktion                                   | BESCHREIBUNG                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Erstellt einen Mailslot und gibt ein mailslot-Handle zurück.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Ruft die maximale Nachrichtengröße, die Maillotgröße, die Größe der nächsten Nachricht im maillot, die Anzahl der Nachrichten im maillot und die Zeitspanne ab, die ein Lesevorgang auf eine Nachricht warten kann. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Ändert das Lesetime out für ein Maillot.                                                                                                                                                                    |



 

Die folgenden Funktionen werden auch von maillot-Servern verwendet.



| Funktion                                                         | BESCHREIBUNG                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Dupliziert das mailslot-Handle.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Ruft Nachrichten aus einem Maillot ab.                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Ruft das Datum und die Uhrzeit der Erstellung eines Maillots ab. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Legt das Datum und die Uhrzeit der Erstellung eines Maillots fest.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Ruft Eigenschaften des mailslot-Handles ab.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Legt Eigenschaften des mailslot-Handles fest.             |



 

## <a name="mailslot-client-functions"></a>Maillot-Clientfunktionen

Ein Clientprozess verwendet bei der Interaktion mit einem Maillot die folgenden Funktionen.



| Funktion                                                             | BESCHREIBUNG                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**Closehandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Schließt ein mailslot-Handle für einen Clientprozess.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Erstellt ein mailslot-Handle für einen Clientprozess. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Dupliziert ein mailslot-Handle.                   |
| [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Schreibt Daten in einen Mailslot.                      |



 

 

 
