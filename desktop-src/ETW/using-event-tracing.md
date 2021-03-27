---
description: In den folgenden Themen wird beschrieben, wie die ETW-API für die Ereignis Ablauf Verfolgung verwendet wird.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Verwenden der Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214865"
---
# <a name="using-event-tracing"></a><span data-ttu-id="26fc4-103">Verwenden der Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="26fc4-103">Using Event Tracing</span></span>

<span data-ttu-id="26fc4-104">In den folgenden Themen wird beschrieben, wie die ETW-API für die Ereignis Ablauf Verfolgung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26fc4-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="26fc4-105">Thema</span><span class="sxs-lookup"><span data-stu-id="26fc4-105">Topic</span></span>                                                                          | <span data-ttu-id="26fc4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26fc4-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26fc4-107">Steuern von Ereignis Ablauf Verfolgungs Sitzungen</span><span class="sxs-lookup"><span data-stu-id="26fc4-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="26fc4-108">Beschreibt, wie Ereignis Ablauf Verfolgungs Sitzungen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="26fc4-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="26fc4-109">Bereitstellen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="26fc4-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="26fc4-110">Beschreibt, wie ein Ereignis Ablauf Verfolgungs Anbieter registriert und instrumentiert wird.</span><span class="sxs-lookup"><span data-stu-id="26fc4-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="26fc4-111">Verarbeiten von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="26fc4-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="26fc4-112">Beschreibt, wie Rückruf Funktionen implementiert werden, die zum Verarbeiten und Verarbeiten von Ereignissen aus einer Ablauf Verfolgungs Protokolldatei oder in Echtzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26fc4-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="26fc4-113">Windows-Ablaufverfolgungs-Präprozessor</span><span class="sxs-lookup"><span data-stu-id="26fc4-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="26fc4-114">Bietet einen effizienten Mechanismus zum Protokollieren und Verarbeiten von Ereignissen, die während der Ausführung einer Anwendung oder eines Treibers auftreten.</span><span class="sxs-lookup"><span data-stu-id="26fc4-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="26fc4-115">Schließen Sie die Header Datei "wmistr. h" ein, bevor Sie die Header Datei "evntrace. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="26fc4-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



