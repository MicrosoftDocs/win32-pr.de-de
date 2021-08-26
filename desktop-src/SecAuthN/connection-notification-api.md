---
description: Der Multiple Provider Router (MPR) ruft die Verbindungsbenachrichtigungsfunktionen auf, wenn eine Netzwerkressource verbunden oder getrennt wird. Um solche Benachrichtigungen zu erhalten, können Sie diese Funktionen in einer DLL implementieren.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: Verbindungs-Benachrichtigungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afaa2e08e6a88f101e8914d9d98a40d6024bdf942ed4bcb0fd1924bc5800213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883310"
---
# <a name="connection-notification-api"></a>Verbindungs-Benachrichtigungs-API

Der [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) ruft die Verbindungsbenachrichtigungsfunktionen auf, wenn eine Netzwerkressource verbunden oder getrennt wird. Um solche Benachrichtigungen zu erhalten, können Sie diese Funktionen in einer DLL implementieren.

Der MPR ruft die [**AddConnectNotify-Funktion**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) vor und nach dem Versuch auf, jeden Add-Connection-Vorgang [**(WNetAddConnection,**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona) [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)oder [**WNetAddConnection3)**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)zu versuchen. Diese Funktion wird nicht aufgerufen, wenn die MPR automatisch Netzwerkverbindungen wiederhergestellt.

Die MPR ruft die [**CancelConnectNotify-Funktion**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) vor und nach dem Versuch auf, jeden Cancel-Connection-Vorgang [**(WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) oder [**WNetCancelConnection2) abzubrechen.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)

Weitere Informationen zu WNET-Funktionen finden Sie unter [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).

Weitere Informationen zum Erstellen und Registrieren einer Anwendung, die Netzwerkverbindungsbenachrichtigungen empfängt, finden Sie unter [Empfangen von Verbindungsbenachrichtigungen](receiving-connection-notifications.md) und [Registrieren zum Empfangen von Verbindungsbenachrichtigungen.](registering-to-receive-connection-notifications.md)

 

 
