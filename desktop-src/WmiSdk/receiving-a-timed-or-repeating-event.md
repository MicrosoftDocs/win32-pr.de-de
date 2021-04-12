---
description: Ein Zeit gesteuerter oder sich wiederholendes Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt oder in regelmäßigen Abständen oder wiederholt auftritt. Ein Ereignis kann z. b. am 2. Dezember 2015 oder einmal wöchentlich um 2:31 Uhr um Mitternacht stattfinden.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Empfangen eines zeitgesteuerten oder wiederholten Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215343"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="6f90c-104">Empfangen eines zeitgesteuerten oder wiederholten Ereignisses</span><span class="sxs-lookup"><span data-stu-id="6f90c-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="6f90c-105">Ein Zeit gesteuerter oder sich wiederholendes Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt oder in regelmäßigen Abständen oder wiederholt auftritt.</span><span class="sxs-lookup"><span data-stu-id="6f90c-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="6f90c-106">Ein Ereignis kann z. b. am 2. Dezember 2015 oder einmal wöchentlich um 2:31 Uhr um Mitternacht stattfinden.</span><span class="sxs-lookup"><span data-stu-id="6f90c-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="6f90c-107">In der folgenden Tabelle werden die verschiedenen Klassen aufgelistet, die zum Erstellen eines zeitgesteuerten oder wiederholten Ereignisses verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f90c-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="6f90c-108">Klasse</span><span class="sxs-lookup"><span data-stu-id="6f90c-108">Class</span></span>                                                                                            | <span data-ttu-id="6f90c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f90c-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f90c-110">[**Win32 \_ Localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [ **Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="6f90c-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="6f90c-111">Standard mäßiges Microsoft-Ereignis Modell.</span><span class="sxs-lookup"><span data-stu-id="6f90c-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="6f90c-112">Weitere Informationen finden Sie unter [Erstellen eines Zeit Geber Ereignisses mit Win32 \_ localtime oder Win32 \_ utcTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="6f90c-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="6f90c-113">**\_\_Timerinstruction**</span><span class="sxs-lookup"><span data-stu-id="6f90c-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="6f90c-114">Legacy-Technik.</span><span class="sxs-lookup"><span data-stu-id="6f90c-114">Legacy technique.</span></span><br/> <span data-ttu-id="6f90c-115">Weitere Informationen finden Sie unter [Erstellen eines Zeit Geber Ereignisses mit \_ timerinstruction](creating-a-timer-event-with---timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="6f90c-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="6f90c-116">Wenn Sie planen, dass ein Task oder ein Auftrag zu einem bestimmten Zeitpunkt oder wiederholt ausgeführt wird, verwenden Sie die [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) -Klasse und ihre Methoden.</span><span class="sxs-lookup"><span data-stu-id="6f90c-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="6f90c-117">Diese Klasse stellt einen Auftrag dar, der mit dem AT-Befehl in einem Befehlsfenster von **Start** und dann **Ausführen** oder über die **geplanten Aufgaben** in der **Systemsteuerung** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f90c-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

