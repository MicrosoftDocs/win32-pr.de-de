---
description: Einige Anwendungen müssen vor dem Auftreten des Ereignisses, unmittelbar nach auftreten oder beides, eine Benachrichtigung über Verbindungs Ereignisse erhalten. Sie können eine DLL erstellen, um die Benachrichtigung über Verbindungs Ereignisse vor und nach der Benachrichtigung zu erhalten.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Empfangen von Verbindungs Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524875"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="b799c-104">Empfangen von Verbindungs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b799c-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="b799c-105">Einige Anwendungen müssen vor dem Auftreten des Ereignisses, unmittelbar nach auftreten oder beides, eine Benachrichtigung über Verbindungs Ereignisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="b799c-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="b799c-106">Sie können eine DLL erstellen, um die Benachrichtigung über Verbindungs Ereignisse vor und nach der Benachrichtigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b799c-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="b799c-107">Ein Beispiel für eine Anwendung, die eine vorab Benachrichtigung über ein Verbindungs Ereignis erhalten muss, ist der RAS-Dienst (RAS).</span><span class="sxs-lookup"><span data-stu-id="b799c-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="b799c-108">RAS muss vor dem Herstellen einer Verbindung informiert werden, da es möglicherweise erforderlich ist, eine Modemverbindung herzustellen, bevor die Netzwerkverbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b799c-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="b799c-109">Ebenso müssen Anwendungen nach dem Herstellen der Verbindung möglicherweise Ressourcen bereinigen, sodass eine Benachrichtigung nach der Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b799c-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="b799c-110">Anwendungen, die voraus-und nachher-Benachrichtigung über Verbindungs Ereignisse erhalten möchten, müssen eine DLL bereitstellen, die zwei Funktionen, [**addconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) und [**cancelconnectnotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify), exportiert.</span><span class="sxs-lookup"><span data-stu-id="b799c-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="b799c-111">Nachdem Sie diese Funktionen implementiert haben, müssen Sie die dll registrieren, wie unter [registrieren für den Empfang von Verbindungs Benachrichtigungen](registering-to-receive-connection-notifications.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b799c-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



