---
title: Richtlinien für Hintergrundaufgaben in Remotedesktopdienste
description: Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben bei der Ausführung in einer Remotedesktopdienste Umgebung, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338981"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a><span data-ttu-id="10a63-103">Richtlinien für Hintergrundaufgaben in Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="10a63-103">Guidelines for background tasks in Remote Desktop Services</span></span>

<span data-ttu-id="10a63-104">Hintergrundaufgaben – Aufgaben, die ausgeführt werden, wenn sich die Nachrichten Schleife einer Anwendung im Leerlauf befindet – bieten einen Mechanismus zum Verarbeiten von Aufgaben mit niedriger Priorität in einer Einzelbenutzer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="10a63-104">Background tasks—tasks performed when an application's message loop is idle—provide a mechanism for handling low-priority tasks in a single-user environment.</span></span> <span data-ttu-id="10a63-105">In einer Remotedesktopdienste Umgebung wird jedoch der Hintergrund Task eines Benutzers für CPU-Zyklen mit den Vordergrund Aufgaben eines anderen Benutzers in den Vordergrund gesetzt.</span><span class="sxs-lookup"><span data-stu-id="10a63-105">In a Remote Desktop Services environment, however, one user's background task competes for CPU cycles with another user's foreground tasks.</span></span> <span data-ttu-id="10a63-106">Wenn mehrere Benutzer sowohl Vordergrund-als auch Hintergrundaufgaben ausführen, sind die CPU-Anforderungen deutlich höher, als wenn alle Benutzer nur Vordergrund Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="10a63-106">When multiple users are running both foreground and background tasks, the CPU demands are much higher than when all users are running only foreground tasks.</span></span> <span data-ttu-id="10a63-107">Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben bei der Ausführung in einer Remotedesktopdienste Umgebung, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.</span><span class="sxs-lookup"><span data-stu-id="10a63-107">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

<span data-ttu-id="10a63-108">Weitere Informationen finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="10a63-108">For more information, see [Detecting the Remote Desktop Services environment](detecting-the-terminal-services-environment.md).</span></span> <span data-ttu-id="10a63-109">Nachdem Sie die Remotedesktopdienste Umgebung erkannt haben, können Sie Hintergrundaufgaben für die Anwendung mit demselben Satz von APIs, die Sie zum Verwalten der Tasks verwendet haben, deaktivieren oder neu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="10a63-109">After you detect the Remote Desktop Services environment, you can disable or reconfigure background tasks for the application using the same set of APIs that you used to manage the tasks.</span></span>

 

 




