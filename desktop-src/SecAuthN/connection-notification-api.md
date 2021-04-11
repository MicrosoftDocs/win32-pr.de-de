---
description: Der multianbieterrouter (MPR) Ruft die Verbindungs Benachrichtigungsfunktionen auf, wenn er eine Netzwerkressource verbindet oder trennt. Um solche Benachrichtigungen zu empfangen, können Sie diese Funktionen in einer DLL implementieren.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: Verbindungs Benachrichtigungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131057"
---
# <a name="connection-notification-api"></a>Verbindungs Benachrichtigungs-API

Der [*multianbieterrouter*](/windows/desktop/SecGloss/m-gly) (MPR) Ruft die Verbindungs Benachrichtigungsfunktionen auf, wenn er eine Netzwerkressource verbindet oder trennt. Um solche Benachrichtigungen zu empfangen, können Sie diese Funktionen in einer DLL implementieren.

Die MPR Ruft die [**addconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) -Funktion vor und nach jedem Vorgang zum Hinzufügen einer Verbindung auf ([**wnetaddconnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)oder [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Diese Funktion wird nicht aufgerufen, wenn die MPR automatisch Netzwerkverbindungen wiederherstellt.

Die MPR Ruft die [**cancelconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) -Funktion vor und nach dem Versuch eines Abbrechen-Connection-Vorgangs ([**wnetcancelconnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) oder [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)) auf.

Weitere Informationen zu WNET-Funktionen finden Sie unter [Windows-Netzwerke](/windows/desktop/WNet/windows-networking-wnet-).

Weitere Informationen zum Erstellen und Registrieren einer Anwendung, die Netzwerk Verbindungs Benachrichtigungen empfängt, finden Sie unter [empfangen von Verbindungs Benachrichtigungen](receiving-connection-notifications.md) und [registrieren für den Empfang von Verbindungs Benachrichtigungen](registering-to-receive-connection-notifications.md).

 

 
