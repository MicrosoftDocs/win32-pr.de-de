---
title: Leistungsrichtlinien
description: Richtlinien für die Entwicklung von Anwendungen, die in einer Remotedesktopdienste Umgebung eine gute Leistung erbringen.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388727"
---
# <a name="performance-guidelines"></a><span data-ttu-id="98da5-103">Leistungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="98da5-103">Performance guidelines</span></span>

<span data-ttu-id="98da5-104">In den folgenden Abschnitten finden Sie Richtlinien zum Entwickeln von Anwendungen, die in einer Remotedesktopdienste Umgebung eine gute Leistung bieten.</span><span class="sxs-lookup"><span data-stu-id="98da5-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98da5-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="98da5-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="98da5-106">Grafische Effekte</span><span class="sxs-lookup"><span data-stu-id="98da5-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="98da5-107">Eine Liste der Funktionen, die beim Ausführen als Remote Sitzung in einer Remotedesktopdienste Umgebung deaktiviert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="98da5-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="98da5-108">Richtlinien für Hintergrundaufgaben in Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="98da5-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="98da5-109">Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben bei der Ausführung in einer Remotedesktopdienste Umgebung, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.</span><span class="sxs-lookup"><span data-stu-id="98da5-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="98da5-110">Verwendung von Threads</span><span class="sxs-lookup"><span data-stu-id="98da5-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="98da5-111">Sie sollten die Anwendungs Thread Verwendung für eine mehr Benutzer-, multiprozessorRemotedesktopdienste Umgebung optimieren und ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="98da5-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="98da5-112">Erkennen der Remotedesktopdienste Umgebung</span><span class="sxs-lookup"><span data-stu-id="98da5-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="98da5-113">Um die Leistung zu optimieren, empfiehlt es sich, Anwendungen zu erkennen, ob Sie in einer Remotedesktopdienste Client Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="98da5-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="98da5-114">Überprüfen Sie die Anwendung auf Speicher Verluste, und beheben Sie etwaige Probleme.</span><span class="sxs-lookup"><span data-stu-id="98da5-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="98da5-115">Dies ist natürlich ein guter Rat für jede Anwendung, aber in einer Remotedesktopdienste Umgebung kann eine Anwendung mehrmals von mehreren Benutzern ausgeführt werden, wodurch die Auswirkungen eines Speicherlecks schnell vergrößert werden.</span><span class="sxs-lookup"><span data-stu-id="98da5-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="98da5-116">Animationen, große Bilder, Audiodaten und andere bandbreitenintensive Dienste müssen konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="98da5-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="98da5-117">Wenn diese Dienste nicht die primäre Funktion sind, können Sie für Remote Sitzungen standardmäßig deaktiviert sein. Sie können jedoch aktiviert werden, wenn eine Sitzung lokal oder über eine Verbindung mit hoher Bandbreite ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98da5-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="98da5-118">Wenn der Zweck einer Anwendung darin besteht, Dienste mit hoher Bandbreite (z. b. Streaming-Videoübertragungen) bereitzustellen, muss der Dienst nicht standardmäßig deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="98da5-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




