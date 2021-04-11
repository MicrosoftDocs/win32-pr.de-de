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
# <a name="connection-notification-api"></a><span data-ttu-id="1306c-104">Verbindungs Benachrichtigungs-API</span><span class="sxs-lookup"><span data-stu-id="1306c-104">Connection Notification API</span></span>

<span data-ttu-id="1306c-105">Der [*multianbieterrouter*](/windows/desktop/SecGloss/m-gly) (MPR) Ruft die Verbindungs Benachrichtigungsfunktionen auf, wenn er eine Netzwerkressource verbindet oder trennt.</span><span class="sxs-lookup"><span data-stu-id="1306c-105">The [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the connection notification functions when it connects or disconnects a network resource.</span></span> <span data-ttu-id="1306c-106">Um solche Benachrichtigungen zu empfangen, können Sie diese Funktionen in einer DLL implementieren.</span><span class="sxs-lookup"><span data-stu-id="1306c-106">To receive such notifications, you can implement these functions in a DLL.</span></span>

<span data-ttu-id="1306c-107">Die MPR Ruft die [**addconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) -Funktion vor und nach jedem Vorgang zum Hinzufügen einer Verbindung auf ([**wnetaddconnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)oder [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span><span class="sxs-lookup"><span data-stu-id="1306c-107">The MPR calls the [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) function before and after attempting each add-connection operation ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a), or [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span></span> <span data-ttu-id="1306c-108">Diese Funktion wird nicht aufgerufen, wenn die MPR automatisch Netzwerkverbindungen wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="1306c-108">This function is not called when the MPR is automatically restoring network connections.</span></span>

<span data-ttu-id="1306c-109">Die MPR Ruft die [**cancelconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) -Funktion vor und nach dem Versuch eines Abbrechen-Connection-Vorgangs ([**wnetcancelconnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) oder [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)) auf.</span><span class="sxs-lookup"><span data-stu-id="1306c-109">The MPR calls the [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) function before and after attempting each cancel-connection operation ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) or [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span></span>

<span data-ttu-id="1306c-110">Weitere Informationen zu WNET-Funktionen finden Sie unter [Windows-Netzwerke](/windows/desktop/WNet/windows-networking-wnet-).</span><span class="sxs-lookup"><span data-stu-id="1306c-110">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span>

<span data-ttu-id="1306c-111">Weitere Informationen zum Erstellen und Registrieren einer Anwendung, die Netzwerk Verbindungs Benachrichtigungen empfängt, finden Sie unter [empfangen von Verbindungs Benachrichtigungen](receiving-connection-notifications.md) und [registrieren für den Empfang von Verbindungs Benachrichtigungen](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1306c-111">For more information about how to create and register an application that receives network connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md) and [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 
