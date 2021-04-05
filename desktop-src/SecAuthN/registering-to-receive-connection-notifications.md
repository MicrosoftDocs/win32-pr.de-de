---
description: Nachdem Sie eine DLL für den Empfang von Verbindungs Benachrichtigungen erstellt haben, müssen Sie Sie beim System registrieren.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrieren für den Empfang von Verbindungs Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756421"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="466c7-103">Registrieren für den Empfang von Verbindungs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="466c7-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="466c7-104">Nachdem Sie eine DLL für den Empfang von Verbindungs Benachrichtigungen erstellt haben, müssen Sie Sie beim System registrieren.</span><span class="sxs-lookup"><span data-stu-id="466c7-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="466c7-105">Hierzu fügen Sie den Wert " **reg \_ Expand \_ SZ** " unter der</span><span class="sxs-lookup"><span data-stu-id="466c7-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="466c7-106">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **notififyees**</span><span class="sxs-lookup"><span data-stu-id="466c7-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="466c7-107">.</span><span class="sxs-lookup"><span data-stu-id="466c7-107">key.</span></span> <span data-ttu-id="466c7-108">Dieser Wert gibt den Pfad zu der dll an, die die [Verbindungs Benachrichtigungs-API](connection-notification-api.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="466c7-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="466c7-109">Der Wert kann einen beliebigen Namen haben.</span><span class="sxs-lookup"><span data-stu-id="466c7-109">The value can have any name.</span></span> <span data-ttu-id="466c7-110">Alle Werte unter dem Schlüssel **notifyees** werden als Pfade zu DLLs behandelt, die über Verbindungs Ereignisse benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="466c7-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="466c7-111">Es wird empfohlen, einen Namen zu verwenden, der die DLL identifiziert.</span><span class="sxs-lookup"><span data-stu-id="466c7-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="466c7-112">Dies verringert die Wahrscheinlichkeit eines Namens Konflikts mit anderen Verbindungs Benachrichtigungs Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="466c7-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="466c7-113">Weitere Informationen zum Erstellen einer Anwendung, die Verbindungs Benachrichtigungen empfängt, finden Sie unter [empfangen von Verbindungs Benachrichtigungen](receiving-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="466c7-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



