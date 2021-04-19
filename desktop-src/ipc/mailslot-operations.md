---
description: Beschreibungen von Funktionen, die bei der Arbeit mit Postfächern, Clients und Servern verwendet werden sollen.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Mailslotvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373080"
---
# <a name="mailslot-operations"></a>Mailslotvorgänge

Bei der Arbeit mit Postfächern sollten Clients und Server nur die Funktionen verwenden, die in den folgenden Tabellen erläutert werden. Verwenden Sie keine anderen Funktionen, auch wenn Sie Datei Handles oder Dateinamen als Parameter akzeptieren, da Sie nicht für die Arbeit mit Postfächern konzipiert sind.

## <a name="mailslot-server-functions"></a>Mailslot-Server Funktionen

Mailslot-Server verwenden die exklusive Verwendung von drei Funktionen, wie in der folgenden Tabelle dargestellt.



| Funktion                                   | BESCHREIBUNG                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatemailslot"**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Erstellt einen Mailslot und gibt ein Mailslot-Handle zurück.                                                                                                                                                            |
| [**Getmailslotinfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Ruft die maximale Nachrichtengröße, die mailslotgröße, die Größe der nächsten Nachricht im postslot, die Anzahl der Nachrichten im Post Slot und die Zeitspanne ab, die ein Lesevorgang auf eine Nachricht warten kann. |
| [**Setmailslotinfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Ändert das Lese Timeout für einen postslot.                                                                                                                                                                    |



 

Die folgenden Funktionen werden auch von Mail Slot-Servern verwendet.



| Funktion                                                         | BESCHREIBUNG                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**Duplialisiehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Dupliziert das Mailslot-handle.                     |
| " [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)", " [ **infofileex** "](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Ruft Nachrichten aus einem postslot ab.                 |
| [**' GetFileTime '**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Ruft das Datum und die Uhrzeit der Erstellung eines postslots ab. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Legt das Datum und die Uhrzeit der Erstellung eines postslots fest.      |
| [**Gethandleinformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Ruft die Eigenschaften des Mailslot-Handles ab.        |
| [**"Ableinformation"**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Legt die Eigenschaften des postslothandles fest.             |



 

## <a name="mailslot-client-functions"></a>Mailslot-Client Funktionen

Ein Client Prozess verwendet die folgenden Funktionen, wenn er mit einem postslot interagiert.



| Funktion                                                             | BESCHREIBUNG                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Schließt ein mailslothandle für einen Client Prozess.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Erstellt ein mailslothandle für einen Client Prozess. |
| [**Duplialisiehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Dupliziert ein Mailslot-handle.                   |
| " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)", " [ **Write fileex** "](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Schreibt Daten in einen postslot.                      |



 

 

 
