---
title: Informations Benachrichtigungen
description: Bei den Verbindungs Zuständen, die als Running States bezeichnet werden, ist keine Aktion für den Benachrichtigungs Handler erforderlich, es sei denn, ein Fehler tritt auf
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "104472397"
---
# <a name="informational-notifications"></a><span data-ttu-id="84f6b-103">Informations Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="84f6b-103">Informational Notifications</span></span>

<span data-ttu-id="84f6b-104">Bei den [Verbindungs Zuständen](connection-states.md) , die als Running States bezeichnet werden, ist keine Aktion für den Benachrichtigungs Handler erforderlich, es sei denn, ein Fehler tritt auf</span><span class="sxs-lookup"><span data-stu-id="84f6b-104">For the [connection states](connection-states.md) known as running states, no action is required of the notification handler unless an error occurs.</span></span> <span data-ttu-id="84f6b-105">Die Ausführung von Zuständen erfolgt bei den Teilen des Verbindungs Vorgangs, die RAS automatisch verarbeitet, z. b. beim Herstellen einer Verbindung mit den erforderlichen Geräten, beim Authentifizieren des Benutzers und beim Warten auf einen Rückruf vom Remote Server.</span><span class="sxs-lookup"><span data-stu-id="84f6b-105">Running states occur during the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="84f6b-106">Bei der Benachrichtigung handelt es sich lediglich um einen Fortschrittsbericht an den Client.</span><span class="sxs-lookup"><span data-stu-id="84f6b-106">The notification is simply a progress report to the client.</span></span>

<span data-ttu-id="84f6b-107">Der Client kann diese Informations Benachrichtigungen an den Benutzer übergeben.</span><span class="sxs-lookup"><span data-stu-id="84f6b-107">The client can choose to pass these informational notifications on to the user.</span></span> <span data-ttu-id="84f6b-108">In einigen ausgelaufenden Zuständen möchte der Client möglicherweise zusätzliche Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="84f6b-108">In some running states, the client may want to display additional information.</span></span> <span data-ttu-id="84f6b-109">Ein Benachrichtigungs Handler, der eine rascs \_ connectdevice-Benachrichtigung empfängt, kann beispielsweise die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " aufrufen, um den Namen und den Typ des Geräts abzurufen, mit dem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="84f6b-109">For example, a notification handler that receives a RASCS\_ConnectDevice notification can call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the name and type of the device being connected to.</span></span> <span data-ttu-id="84f6b-110">Ein weiteres Beispiel ist, wenn der Client eine in rascs \_ projizierte Benachrichtigung empfängt.</span><span class="sxs-lookup"><span data-stu-id="84f6b-110">Another example is when the client receives a RASCS\_Projected notification.</span></span> <span data-ttu-id="84f6b-111">Dies tritt auf, wenn die RAS-Projektionsphase des Verbindungs Vorgangs abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="84f6b-111">This occurs when the RAS projection phase of the connection operation has been completed.</span></span> <span data-ttu-id="84f6b-112">Der Client kann die Funktion " [**rasgetprojectioninfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) " aufrufen, um zusätzliche Informationen über die Projektion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="84f6b-112">The client can call the [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) function to get additional information about the projection.</span></span> <span data-ttu-id="84f6b-113">Der Client kann diese Informationen verwenden, um den Benutzer darüber zu benachrichtigen, welche Netzwerkprotokolle von dieser Verbindung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="84f6b-113">The client can use this information to notify the user as to which network protocols can be used by this connection.</span></span>

<span data-ttu-id="84f6b-114">Sie sollten vermeiden, Code zu schreiben, der von der Reihenfolge oder dem Vorkommen bestimmter Informations Zustände abhängt, da dies zwischen den Plattformen variieren kann.</span><span class="sxs-lookup"><span data-stu-id="84f6b-114">You should avoid writing code that depends on the order or occurrence of particular informational states, because this may vary between platforms.</span></span>

 

 




